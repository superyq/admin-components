<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          ring-one-echarts(
            cId="demo",
            :xDatas='xDatas',
            :colorArr='[color1,color2,color3,color4,color5,color6]'
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
          b 1、cId：
          | echarts的Id，每个echarts组件id不同，必传
        
        p 
          b 2、colorArr：[{{ color1 }},{{ color2 }},{{ color3 }},{{ color4 }},{{ color5 }},{{ color6 }},]：
          | echarts的Id，每个echarts组件id不同，必传
        .page-control_control.c-c
          span 颜色1：
          el-color-picker(v-model="color1")
          span ，颜色2：
          el-color-picker(v-model="color2")
          span ，颜色3：
          el-color-picker(v-model="color3")
          span ，颜色4：
          el-color-picker(v-model="color4")
          span ，颜色5：
          el-color-picker(v-model="color5")
          span ，颜色6：
          el-color-picker(v-model="color6")
        
        p 
          b 3、xDatas: {{ xDatas }}：
          | 柱状图数据，数据格式如例。
        
        
</template>
<script>
export default {
  name: "yq-ringone",
  data() {
    return {
      htmlData: `<ring-one-echarts cId='demo' :colorArr='colors' :xDatas='datas'></ring-one-echarts>`,
      xDatas: [
        { name: "周一", number: 10 },
        { name: "周一", number: 10 },
        { name: "周一", number: 10 },
        { name: "周一", number: 10 },
        { name: "周一", number: 10 },
        { name: "周一", number: 10 },
      ],
      colors: ["#3F06F8", "#5AD8A6", "#F6BD16", "#5b8ff9", "#E86452", "#9E03FF"],
      color1: "#3F06F8",
      color2: "#5AD8A6",
      color3: "#F6BD16",
      color4: "#5b8ff9",
      color5: "#E86452",
      color6: "#9E03FF",
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
