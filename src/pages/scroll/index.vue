<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-look_box
          c-scroll(@toBottom='toBottom', :rem='rem')
            .demo-table
              .demo-table_item(v-for='item in 20') {{ item }}
                

      .page-coder
        .page-coder_title 使用
        .page-coder_content {{ htmlData }}
          
    .page-control
      .page-control_title 参数详解
      .page-control_content
        p 
          b 注意：
          | 父级容器需设置宽高和overflow: hidden;子集盒子宽度需要设置 width: calc(100% - 0.5rem)或者 width: calc(100% - 50px)
      
        p 
          b rem: {{ rem }}，
          | 圆角是否使用rem单位, true:是, false: 否, 默认为false
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
        
</template>
<script>
export default {
  name: "yq-scroll",
  data() {
    return {
      htmlData: `<c-scroll @toBottom='toBottom' :rem='false'>
      <table></table>
      </c-scroll>`,
      rem: false,
    };
  },
  methods: {
    toBottom() {
      console.log("toBottom");
    },
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
