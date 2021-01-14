<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          line-one-echarts(
            cId="demo",
            :color='color',
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
          b color: {{ color }}，
          | 线型图的下部颜色
        .page-control_control
          
      
        p 
          b xDatas: {{ xDatas }}，
          | 线性图数据
        .page-control_control
        
        p 
          b xName: {{ xName }}，
          | 线性图命名
        .page-control_control
        
</template>
<script>
export default {
  name: "yq-lineone",
  data() {
    return {
      htmlData: `<line-one-echarts cId="demo" :color='color' :xDatas="xDatas" :xName='xName'></line-one-echarts>`,
      color: ["blue", "yellow"],
      xName: ["1月", "2月"],
      xDatas: [820, 932],
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
