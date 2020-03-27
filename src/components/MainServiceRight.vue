<template>
  <div class="mainServiceRight">
      <div class="top">
        <div style="font-weight:bold">Current</div>
        <div>
          <span>View all</span> 
        </div>
      </div>
      <div class="content" v-for="item in [1,2,3]" :key="item">
        <div class="padRight">106387132456</div>
        <div class="borderBottom"></div>
        <div class="padLeft">$202124.11</div>
      </div>
      <div class="top" style="margin-top:30px;">
        <div style="font-weight:bold">Savings</div>
        <div>
          <span>View all</span> 
        </div>
      </div>
      <div class="mapBox">
        <div id="myChart" style="max-width:500px;width:100%;height:250px;"></div>
        <div style="margin-top:50px;width:200px;">
          <div class="mapRight">
            <div style="color: gray">Total</div>
            <div style="font-weight:bold;">$100.09</div>
          </div>
          <div class="mapRight">
            <div style="color: gray">This week</div>
            <div style="font-weight:bold;">$100123.09</div>
          </div>
          <div class="mapRight">
            <div style="color: gray">This month</div>
            <div style="font-weight:bold;">$1012320.09</div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
let echarts = require('echarts/lib/echarts')
require('echarts/lib/chart/line')
require('echarts/lib/chart/pie')
// 以下的组件按需引入
require('echarts/lib/component/tooltip')   // tooltip组件
require('echarts/lib/component/title')   //  title组件
require('echarts/lib/component/legend') 
export default {
  data(){
    return {
      
    }
  },
  methods:{
    initMap(){
      let myChart = echarts.init(document.getElementById('myChart'))
      myChart.setOption({
        xAxis: {
            type: 'category',
            data: ['$10', '$20', '$30', '$40', '$50']
        },
        yAxis: {
            type: 'value'
        },
        series: [{
            data: [1/100, 15/100, 7/100, 27/100, 15/100 ],
            type: 'line'
        }]
      })
    },
  },
  mounted(){
    this.initMap()
  }
}
</script>

<style scoped>
.mapBox{
  width: 100%;
  display: flex;
  justify-content: space-between;
}
.mapRight{
  width: 200px;
  font-size: 14px;
  display:flex;
  justify-content: space-between;
}
.mainServiceRight{
  padding: 0 50px;
}
.top{
  display: flex;
  justify-content: space-between;
}
.top>div>span{
  color: gray;
  font-size: 12px;
}
.borderBottom{
  border-bottom: 2px dashed gray;
  flex: 1;
}
.content{
  display:flex;
  align-items: flex-end;
  margin-top: 20px;
}
.padLeft{
  padding-left: 40px;
  font-weight: bold;
  font-size: 14px;
}
.padRight{
  padding-right: 40px;
  color: gray;
  font-size: 14px;
}
</style>