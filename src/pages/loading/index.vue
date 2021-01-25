<template lang='pug'>
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-loading_box
          c-loading(:loading='loading', :rem='rem')
      .page-coder
        .page-coder_title 使用
        .page-coder_content {{ htmlData }}

    .page-control
      .page-control_title 参数详解
      .page-control_content
        p 
          b 注意：
          | 大小由外部盒子决定，外部盒子需设置 position: relative

        p 
          b 1、loading: {{ loading }}：
          | 判断是否显示加载中, true:显示, false:隐藏, 默认为false
        .page-control_control
          el-switch(
            v-model="loading"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )

        p 
          b 2、rem: {{ rem }}：
          | 加载圈是否使用rem单位, true:是, false: 否, 默认为true
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
</template>
<script>
export default {
  name: 'yq-loading',
  data() {
    return {
      htmlData: `<c-loading :loading='true' :rem='false'></c-loading>`,
      loading: false,
      rem: false
    }
  }
}
</script>
<style lang='scss'>
@import "./index.scss";
</style>