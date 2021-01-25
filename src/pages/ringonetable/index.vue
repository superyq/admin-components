<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          ring-one-table(
            cId="demo",
            :rem='rem',
            :colorArr='colors',
            :obj='obj'
          )
            .table(style='border: 1px solid') 表格样式自定义
          
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
          | 整体布局是否使用rem单位，false：否，true：是，默认为true
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
      
        p 
          b 3、colorArr: {{ colors }}：
          | 圆环颜色

        p 
          b 4、obj: {{ obj }}：
          | 柱状图数据，数据格式如例。
        
        
</template>
<script>
export default {
  name: "yq-ringonetable",
  data() {
    return {
      htmlData: `<ring-one-table cId='demo' :rem='rem' :colorArr='colors' :obj='obj'></ring-one-table>`,
      rem: false,
      colors: ["#3F06F8", "#5AD8A6", "#F6BD16", "#5b8ff9", "#E86452", "#9E03FF"],
      obj: {
        title: "标题",
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
