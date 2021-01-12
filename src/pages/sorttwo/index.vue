<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-percent_box
          c-percentage(
            :width='`${width}%`',
            :background="[colorStart, colorEnd]",
            :haveBg="haveBg", 
            :rem="rem"
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
          b width: {{ width }}%，
          | 进度条百分比, 0%-100%, 默认为50%
        .page-control_control
          el-slider(v-model='width')
      
        p 
          b background: [{{ colorStart }}, {{ colorEnd }}]，
          | 进度条颜色左到右, 默认为["#002adb", "#04f7fb"]
        .page-control_control.c-c
          span 开始颜色：
          <el-color-picker v-model="colorStart"></el-color-picker>
          span ，结束颜色：
          <el-color-picker v-model="colorEnd"></el-color-picker>
        
        p 
          b haveBg: {{ haveBg }}，
          | 是否显示黑色背景, true:是, false: 否, 默认为true
        .page-control_control.c-c 
          el-switch(
            v-model="haveBg"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )

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
  name: "yq-sorttwo",
  data() {
    return {
      htmlData: `<c-percentage width='70%' :background='["#002adb", "#04f7fb"]' :haveBg='false' rem></c-percentage>`,
      width: 50,
      colorStart: "#002adb",
      colorEnd: "#04f7fb",
      haveBg: true,
      rem: false
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
