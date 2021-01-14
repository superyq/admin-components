<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          ring-one-table(
            cId="demo",
            :obj='obj'
          )
            .table
              .table-item(v-for='item in 5') {{ item }}
          
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
          b xDatas: {{ xDatas }}，
          | 圆环图数据
        .page-control_control
          
      
        p 
          b colorArr: {{ colorArr }}，
          | 圆环图颜色
        .page-control_control
        
        
</template>
<script>
export default {
  name: "yq-radarone",
  data() {
    return {
      htmlData: `<ring-one-echarts cId='demo' :colorArr='colors' :xDatas='datas'></ring-one-echarts>`,
      obj: {
        title: "a",
        datas: [
          { name: "周一", number: 10 },
          { name: "周一", number: 10 },
          { name: "周一", number: 10 },
          { name: "周一", number: 10 },
          { name: "周一", number: 10 },
          { name: "周一", number: 10 },
        ],
      },
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
