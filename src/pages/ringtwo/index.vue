<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          ring-two-echarts(
            cId="demo"
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
        
</template>
<script>
export default {
  name: "yq-ringtwo",
  data() {
    return {
      htmlData: `<ring-two-echarts cId='demo'></ring-two-echarts>`,
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
