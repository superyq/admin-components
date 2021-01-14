<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          pie-one-echarts(
            cId="demo",
            :title='title',
            :xName='xName',
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
          b cId，
          | echarts的Id，每个echarts组件id不同

        p 
          b title: {{ title }}，
          | 标题
        .page-control_control
          
      
        p 
          b xDatas: {{ xDatas }}，
          | 柱状图数据，数据格式如例:value: 数值，cValue: 比年初
        .page-control_control
        
        p 
          b xName: {{ xName }}，
          | 柱状图x轴命名, 数据格式如例子
        .page-control_control
        
        p 
          b rem: {{ rem }}，
          | 判断是否使用rem单位
        .page-control_control
        
</template>
<script>
export default {
  name: "yq-pieone",
  data() {
    return {
      htmlData: `<pie-one-echarts cId="demo" :title='title' :xName='xName' :xDatas='xDatas' :rem='rem'></-two-echarts>`,
      title: '标题',
      xName: ["建行", "招行", "工行", "农行", "中行", "交行"],
      xDatas: [
        { value: 10, cValue: "10%" },
        { value: 10, cValue: "10%" },
        { value: 10, cValue: "10%" },
        { value: 10, cValue: "10%" },
        { value: 10, cValue: "10%" },
        { value: 10, cValue: "-10%" },
      ],
      rem: false
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
