<template>
  <div class="page">
          <div class="up" id="up_data">
            <div class="font"><h1>指令详情</h1></div>
            <div class="lines">
              <div class="item1">ID指令</div>
              <div class="item2">{{object.id}}</div>
              <div class="item3">指令类型</div>
              <div class="item4">{{ object.type }}</div>
              <div class="item5">版本号</div>
              <div class="item6">{{ object.version }}</div>
              <div class="item7">指令下发时间</div>
              <div class="item8">{{ object.time }}</div>
              <div class="item9">指令属主</div>
              <div class="item10">{{ object.owner }}</div>
              <div class="item11">指令优先级</div>
              <div class="item12">{{ object.order }}</div>
              <div class="item13">数据上报方式</div>
              <div class="item14">{{ object.reporting_method }}</div>
              <div class="item15">指令描述</div>
              <div class="item16">{{ object.description }}</div>
              <div class="item17">生效运营商</div>
              <div class="item18">{{ object.operator }}</div>
          </div>
        </div>
          <div class="down">
            <div class="stat"><statistic></statistic></div>
          </div>
          <div class="down2">
            <div class="chart"><chart></chart></div>
          </div>
          <div class="down3">
            <div class="table"><commontable></commontable></div>
          </div>
    </div>
  </template>

<script>
import statistic from "./CommonStatistic.vue"
import chart from "./CommonChart.vue"
import commontable from "./CommonTable.vue"
export default {
  components: {
    statistic,
    chart,
    commontable,
  },
  data() {
    return{
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
  <style scoped>
  
.page{
  
  .up {
    height: 300px;
    border-radius: 10px;
    border: 0.5px solid #B3C0D1;
    background-color: #ffffff;
    color: #333;
    line-height: 80px;
    text-align: left;
  } 
  .down{
    margin-top: 10px;
    height: 300px;
    border-radius: 10px;
    background-color: #ffffff;
    border: 0.5px solid #B3C0D1;
    color: #333;
    line-height: 80px;
    text-align: left;
  }
  .down2{
    margin-top: 10px;
    height: 400px;
    border-radius: 10px;
    background-color: #ffffff;
    border: 0.5px solid #B3C0D1;
    color: #333;
    line-height: 80px;
    text-align: left;
  }
  .down3{
    margin-top: 10px;
    height: 400px;
    border-radius: 10px;
    background-color: #ffffff;
    border: 0.5px solid #B3C0D1;
    color: #333;
    line-height: 80px;
    text-align: left;
  }
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
    grid-template-columns:200px 300px 200px 300px 200px 300px ;
    grid-gap: 10px;
  }
}


</style>