<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-percent_box
          sort-two(
            :rem="rem",
            :txt='txt',
            :sort='sort'
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
          b 1、rem: {{ rem }}：
          | 字体是否使用rem单位, true:是, false: 否, 默认为false
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
        
        p 
          b 2、txt: {{ txt }}：
          | 名称
        .page-control_control.page-control_control-input
          el-input(
            placeholder="请输入内容",
            size='mini',
            v-model="txt",
            maxlength='20',
            clearable
          ) 
        
        p 
          b 3、sort: {{ sort }}：
          | 标题名
        .page-control_control.page-control_control-input
          el-input(
            placeholder="请输入内容",
            size='mini',
            v-model="sort",
            maxlength='20',
            clearable
          )
        
</template>
<script>
export default {
  name: "yq-sorttwo",
  data() {
    return {
      htmlData: `<sort-two :rem='rem' :txt='txt' :sort='sort'></sort-two>`,
      rem: false,
      txt: '排名',
      sort: 1
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
