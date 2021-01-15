<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-btn_box
          header-one(
            :rem='rem',
            :type='type',
            :title='title',
            :bgImg="bgImg",
            :cStyle='cStyle'
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
          | 整体布局是否使用rem单位, true:是, false: 否, 默认为false
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
      
        p 
          b 2、type: {{ type }}：
          | 标题样式，有3种，传1，2，3
        .page-control_control.page-control_control-input
          el-input(
            placeholder="请输入内容",
            size='mini',
            type='number'
            v-model="type",
            maxlength='20',
            clearable
          ) 
        
        p 
          b 3、title: {{ title }}：
          | 标题名
        .page-control_control.page-control_control-input
          el-input(
            placeholder="请输入内容",
            size='mini',
            v-model="title",
            maxlength='20',
            clearable
          ) 
        
        p 
          b 4、bgImg：
          | 标题图片
        .page-control_control.page-control_control-input
        
        p 
          b 5、cStyle：{{cStyle}}：
          | 字体样式
        
</template>
<script>
import img from "@/assets/6.jpg";
export default {
  name: "yq-headerone",
  data() {
    return {
      htmlData: `<header-one :rem='rem' :type='type' :title='title' :bgImg="bgImg" :cStyle='cStyle'></header-one>`,
      rem: false,
      type: 1,
      title: '我是标题',
      bgImg: img,
      cStyle: 'font-size: 18px; color: red'
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
