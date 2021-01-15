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
          b 1、cId：
          | echarts的Id，每个echarts组件id不同，必传
      
        p 
          b 2、xName: {{ xName }}：
          | 柱状图x轴命名, 数据格式如例子。

        p 
          b 3、xDatas: {{ xDatas }}：
          | 柱状图数据，数据格式如例。
        
        
        
</template>
<script>
export default {
  name: "yq-radarone",
  data() {
    return {
      htmlData: `<radar-one-echarts cId="demo" :xName='xName' :xDatas='xDatas'></radar-one-echarts>`,
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
