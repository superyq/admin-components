<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          radar-one-echarts(
            cId="demo",
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
          b cId，
          | echarts的Id，每个echarts组件id不同

        p 
          b xName: {{ xName }}，
          | 雷达图X轴
        .page-control_control
          
      
        p 
          b xDatas: {{ xDatas }}，
          | 雷达图数据
        .page-control_control
        
        
</template>
<script>
export default {
  name: "yq-radarone",
  data() {
    return {
      htmlData: `<radar-one-echarts cId="demo" :color='color' :xName='xName' :xDatas='xDatas'></radar-one-echarts>`,
      xName: [
        { name: "经营计划客户覆盖率", max: 50 },
        { name: "核心需求评估客户覆盖率", max: 50 },
        { name: "解决方案客户覆盖率", max: 50 },
        { name: "产品及年度检视报告客户覆盖率", max: 50 },
        { name: "客户关系检视客户覆盖率", max: 50 },
        { name: "经营计划客户覆盖率", max: 50 },
      ],
      xDatas: [43, 10, 28, 35, 50, 10],
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
