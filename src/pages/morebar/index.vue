<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          more-bar-echarts(
            cId="demo",
            :xName='xName',
            :lName='lName',
            :xDatas='xDatas',
            :rem='rem'
          )
          
      .page-coder
        .page-coder_title 使用
        .page-coder_content {{ htmlData }}
          
    .page-control
      .page-control_title 参数详解
      .page-control_content
        p 
          b 注意：
          | 大小由外部盒子决定

        p 
          b 1、cId：
          | echarts的Id，每个echarts组件id不同，必传
        
        p 
          b 2、rem: {{ rem }}：
          | tooptip是否使用rem单位，false：否，true：是，默认为false
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
      
        p 
          b 3、lName: {{ lName }}：
          | 柱状图x轴命名, 数据格式如例子。

        p 
          b 4、xName: {{ xName }}：
          | 柱状图x轴命名, 数据格式如例子。

        p 
          b 5、xDatas: {{ xDatas }}：
          | 柱状图数据，数据格式如例。
        
        
</template>
<script>
export default {
  name: "yq-morebar",
  data() {
    return {
      htmlData: `<more-bar-echarts cId="demo"  :rem='rem' :xName='xName' :lName='lName' xDatas='xDatas'></more-bar-echarts>`,
      rem: false,
      xName: ["北京", "上海", "四川", "重庆", "北京", "上海", "四川", "重庆"],
      lName: ["建行", "招商", "工行", "交通", "农行", "中国"],
      xDatas: [
        {
          name: "建行",
          type: "bar",
          barWidth: "20%",
          stack: "总量",
          label: {
            show: true,
            formatter: "{c} %",
          },
          itemStyle: {
            color: "#3F06F8",
          },
          data: [
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
          ],
        },
        {
          name: "招商",
          type: "bar",
          barWidth: "20%",
          stack: "总量",
          label: {
            show: true,
            formatter: "{c} %",
          },
          itemStyle: {
            color: "#5AD8A6",
          },
          data: [
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
          ],
        },
        {
          name: "工行",
          type: "bar",
          barWidth: "20%",
          stack: "总量",
          label: {
            show: true,
            formatter: "{c} %",
          },
          itemStyle: {
            color: "#9E03FF",
          },
          data: [
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
          ],
        },
        {
          name: "交通",
          type: "bar",
          barWidth: "20%",
          stack: "总量",
          label: {
            show: true,
            formatter: "{c} %",
          },
          itemStyle: {
            color: "#5B8FF9",
          },
          data: [
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
          ],
        },
        {
          name: "农行",
          type: "bar",
          barWidth: "20%",
          stack: "总量",
          label: {
            show: true,
            formatter: "{c} %",
          },
          itemStyle: {
            color: "#F6BD16",
          },
          data: [
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
          ],
        },
        {
          name: "中国",
          type: "bar",
          barWidth: "20%",
          stack: "总量",
          label: {
            show: true,
            formatter: "{c} %",
          },
          itemStyle: {
            color: "#E86452",
          },
          data: [
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
            { value: 10, cValue: "-10%" },
            { value: 15, cValue: "-10%" },
            { value: 30, cValue: "-10%" },
            { value: 20, cValue: "10%" },
          ],
        },
      ],
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
