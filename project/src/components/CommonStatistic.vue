<template>
    <div class="statistic">
        <div class="font"><h1>指令反馈省份统计</h1></div>
        <div class="lines">
              <div class="item1">反馈省份</div>
              <div class="item2" >
                <el-select v-model="value1" placeholder="请选择省份">
                <el-option
                    v-for="item in options"
                   :key="item.value"
                  :label="item.label"
                  :value="item.value">
               </el-option>
               </el-select>
              </div>
              <div class="item3">传输层协议</div>
              <div class="item4">
                <el-select v-model="value2" placeholder="请选择协议类型">
                <el-option
                    v-for="item in options"
                   :key="item.value"
                  :label="item.label"
                  :value="item.value">
               </el-option>
               </el-select></div>
              <div class="item5">事件分类</div>
              <div class="item6">
                <el-select v-model="value3" placeholder="请选择事件大类">
                <el-option
                    v-for="item in options"
                   :key="item.value"
                  :label="item.label"
                  :value="item.value">
               </el-option>
               </el-select></div>
              <div class="item7">源IP</div>
              <div class="item8"> <el-input size="medium"   v-model="input1" placeholder="请输入源IP" ></el-input></div>
              <div class="item9">目的IP</div>
              <div class="item10"> <el-input size="medium"   v-model="input2" placeholder="请输入目的IP"></el-input></div>
              <div class="item11">事件描述</div>
              <div class="item12"> <el-input size="medium"   v-model="input3" placeholder="请输入事件描述"></el-input></div>
              <div class="item13">手机号</div>
              <div class="item14"> <el-input size="medium"   v-model="input4" placeholder="请输入手机号"></el-input></div>
              <div class="item15">IMEI</div>
              <div class="item16"> <el-input size="medium"   v-model="input5" placeholder="请输入IMEI"></el-input></div>
              <div class="item17"><el-button >重置</el-button></div>
              <div class="item18">
                <el-button type="primary" size="meduim">查询</el-button>
                <el-button type="primary">导出</el-button>
              </div>
          </div>
      </div>
</template>
  
<script>
import statistic from "./CommonStatistic.vue"
export default {
  components: {
    statistic,
  },
  data() {
    return{
      input1:'',input2:'',input3:'',input4:'',input5:'',input6:'',input7:'',
      options: [{
          value: '选项1',
          label: '指令1'
        }, {
          value: '选项2',
          label: '指令2'
        }, {
          value: '选项3',
          label: '指令3'
        }, {
          value: '选项4',
          label: '指令4'
        }, {
          value: '选项5',
          label: '指令5'
        }],
        value1: '',
        value2: '',
        value3: '',
    object: {
      id: '000000000000',
      type: '网络资源监测指令',
      version: '2.0',
      time:'2022-07-19 19:17:59',
      owner:'admin',
      order:'高',
      reporting_method:'每30分钟定时报送',
      description:'xxxxxxxxxxxxx',
      operator:'移动、联通、电信、广电'
    }
  }
}
}
</script>
<style>
  
.statistic{
    height: 300px;
    line-height: 80px;
    text-align: left;
  .font{
    font-size: x-large;
    height: 10px;
    line-height: 20px;
    padding: 10px 17px;
    margin-left: -150px;
  }
  .lines{
    margin-left:40px;
    display: grid;
    grid-template-columns:100px 400px 100px 400px 100px 400px ;
    grid-gap: 10px;
  }
  .item2{
    margin-right: 10px;
  }
  .item8{
    margin-right: 80px;
  }
  .item10{
    margin-right: 80px;
  }
  .item12{
    margin-right: 80px;
  }
  .item14{
    margin-right: 80px;
  }
  .item16{
    margin-right: 80px;
  }
 
}


</style>