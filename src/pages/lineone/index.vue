<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          line-one-echarts(
            cId="demo",
            :color='[colorStart, colorEnd]',
            :xName='xName',
            :xDatas='xDatas'
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
          b 2、color: [{{ colorStart }}, {{ colorEnd }}]：
          | 线型图背景色, 默认为["#FF9F05", "rgba(255,159,5,0)"]
        .page-control_control.c-c
          span 开始颜色：
          el-color-picker(v-model="colorStart")
          span ，结束颜色：
          el-color-picker(v-model="colorEnd")
      
        p 
          b 3、xName: {{ xName }}：
          | 柱状图x轴命名, 数据格式如例子。

        p 
          b 4、xDatas: {{ xDatas }}：
          | 柱状图数据，数据格式如例。
                
</template>
<script>
export default {
  name: "yq-lineone",
  data() {
    return {
      htmlData: `<line-one-echarts cId="demo" :color='color' :xName='xName' :xDatas="xDatas"></line-one-echarts>`,
      colorStart: '#FF9F05',
      colorEnd: 'rgba(255,159,5,0)',
      xName: ["1月", "2月", "3月", "4月", "5月", "6月", "7月"],
      xDatas: [820, 932, 901, 934, 1290, 1330, 1320],
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
