<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-look_box
          table-wrapper-one(
            :rem='rem',
            :widthArr='widthArr', 
            :headerArr='headerArr', 
            :datasArr='datasArr', 
            :bottom='bottom', 
            :option='option'
          )

      .page-coder
        .page-coder_title 使用
        .page-coder_content {{ htmlData }}
          
    .page-control
      .page-control_title 参数详解
      .page-control_content
        p 
          b 注意：
          | 大小由外部盒子决定,可以自定义每列的样式

        p 
          b widthArr: {{ widthArr }}，
          | table列表的每列宽度
        .page-control_control
      
        p 
          b headerArr: {{ headerArr }}，
          | table列表的表头标题
        .page-control_control
        
        p 
          b datasArr: {{ datasArr }}，
          | 列表数据
        .page-control_control
        
        p 
          b bottom: {{ bottom }}，
          | 每行距离下方距离
        .page-control_control
        
        p 
          b option: {{ option }}，
          | 查看自动滚动组件配置项
        .page-control_control

</template>
<script>
export default {
  name: "yq-tableone",
  data() {
    return {
      htmlData: `<table-wrapper-one :width='widthArr' :headerArr='headerArr' :datasArr='datasArr' bottom='0.2'></table-wrapper-one>`,
      rem: false,
      widthArr: [2.8, 1.64, 1.5, 1.5, 1],
      headerArr: ["私行占比排名", "私行占比", "系统占比", "期末（私行）", "期末（零售）"],
      datasArr: [{ name: "yq", sort: 1, width: "10", datas: [1, 2, 3] }],
      option: {},
      bottom: "0.2",
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
