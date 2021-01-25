<template lang='pug'>
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        c-master(:text='text' :rem='rem')
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
          b 1、text: {{ text }}：
          | 遮罩层的文字, 默认为"遮罩"
        .page-control_control
          el-input(
            maxlength='10',
            placeholder="请输入内容",
            v-model="text",
            clearable
          )

        p 
          b 2、rem: {{ rem }}：
          | 文字是否使用rem单位, true:是, false: 否, 默认为true
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
</template>
<script>
export default {
  name: 'yq-master',
  data() {
    return {
      htmlData: `<c-master text='遮罩' :rem='false'></c-master>`,
      text: '遮罩',
      rem: false
    }
  }
}
</script>
<style lang='scss'>
@import "./index.scss";
</style>