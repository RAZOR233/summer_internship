<template>
    <div class="header">
    <div class="tag">
    <el-radio-group v-model="tabPosition" >
      <el-radio-button label="jin">今日</el-radio-button>
      <el-radio-button label="right">近7日</el-radio-button>
      <el-radio-button label="bottom">近30日</el-radio-button>
      <el-radio-button label="left">自定义</el-radio-button>
    </el-radio-group>
</div>
<div class="font"><h1>指令ID</h1></div>

<div class="searcher" >
    <el-input size="medium"   v-model="input" placeholder="请输入指令ID"></el-input>
</div>
<div class="font2"><h1>指令类型</h1></div>
<div class="select">
    <el-select v-model="value" placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</div>
<div class="button">
    <el-button >重置</el-button>
    <el-button type="primary">查询</el-button>
</div>

</div>
  </template>
  
  <script>

    export default {
      data() {
        return {
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
        value: '',
          tabPosition: 'left',
          input:''
        };
      }
    };
  </script>
<style>

.header{
    display:flex;
}
.font{
    position:relative;
    left:150px;
}
.font2{
    position:relative;
    left:100px;
}
.tag {
    margin-top: 0px;
    position:relative;
}
.searcher {
    width: 350px;
    display:flex;
    margin-top: 0px;
    margin-left:180px;
    left:200px
}
.select {
    display:flex;
    margin-left:0px;
    position:relative;
    left:140px;
}
.button{
    margin-top: 10px;
    height: 40px;
    display:flex;
    margin-left:0px;
    position:relative;
    left:180px;
}
</style>