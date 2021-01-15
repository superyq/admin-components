<template lang='pug'>
  .page-home
    h1 @yqcoder_components
    
    .page-home_step 
      p 1、安装依赖
      .page-home_step-box npm install @yqcoder/components
    
    .page-home_step 
      p 2、main.js引用依赖
      .page-home_step-box 
        .page-home_step-box import yqComponent from "@yqcoder/components";
        .page-home_step-box Vue.use(yqComponent);

</template>

<script>
export default {
  name: 'page-home'
}
</script>

<style lang='scss'>
@import "./index.scss";
</style>
