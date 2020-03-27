<template>
  <div>
    <div class="rightTop">
      <div class="rightPageIcon">
        <img src="@/assets/lindang.png" alt />
      </div>
      <div class="topFont">
        Anastasia
        <img src="@/assets/logo.png" alt class="img" />
      </div>
    </div>
    <div style="margin:50px 0;">
        <div id="myChart1" style="width:250px;height:250px"></div>
    </div>
  </div>
</template>

<script>
let echarts = require('echarts/lib/echarts')
require('echarts/lib/chart/pie')
// 以下的组件按需引入
require('echarts/lib/component/tooltip')   // tooltip组件
require('echarts/lib/component/title')   //  title组件
export default {
  data() {
    return {};
  },
  methods: {
    initPidMap() {
      let myChart = echarts.init(document.getElementById("myChart1"));
      myChart.setOption({
        tooltip: {
          trigger: "item",
          formatter: "{a} <br/>{b}: {c} ({d}%)"
        },
        
        series: [
          {
            name: "访问来源",
            type: "pie",
            radius: ["50%", "70%"],
            avoidLabelOverlap: false,
            label: {
              show: true,
              position: "center"
            },
            emphasis: {
              label: {
                show: true,
                fontSize: "30",
                fontWeight: "bold"
              }
            },
            labelLine: {
              show: true
            },
            data: [
              { value: 1, name: "" },
              { value: 1, name: "" },
              { value: 1, name: "" },
              { value: 1, name: "视频广告" },
            ]
          }
        ]
      });
    }
  },
  mounted(){
      this.initPidMap()
  }
};
</script>

<style scoped>
.rightTop {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
}
.img {
  width: 30px;
  border-radius: 40px;
  border: 1px solid black;
  vertical-align: middle;
  margin-left: 6px;
}
.topFont {
  font-size: 12px;
  width: 100px;
}
.rightPageIcon {
  min-width: 120px;
}
</style>