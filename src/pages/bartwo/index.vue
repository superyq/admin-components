<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-echarts_box
          bar-two-echarts(
            cId="demo",
            :rem='rem',
            :title="title",
            :xDatas="xDatas"
            :xName='xName'
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
          | echarts的Id，每个echarts组件id不同

        p 
          b 2、title: {{ title }}：
          | 标题
        .page-control_control.page-control_control-input
          el-input(
            placeholder="请输入内容",
            v-model="title",
            maxlength='20',
            clearable
          )
        
        p 
          b 3、rem: {{ rem }}：
          | 标题是否使用rem单位，false：否，true：是，默认为true
        .page-control_control
          el-switch(
            v-model="rem"
            active-color="#13ce66"
            inactive-color="#ff4949"
          )
      
        p 
          b 4、xName: {{ xName }}，
          | 柱状图x轴命名, 数据格式如例。

        p 
          b 5、xDatas: {{ xDatas }}，
          | 柱状图数据，数据格式如例。

</template>
<script>
export default {
  name: "yq-bartwo",
  data() {
    return {
      htmlData: `<bar-two-echarts cId="demo" :title="title" :rem='rem' :xDatas="xDatas" :xName='xName' ></bar-two-echarts>`,
      rem: false,
      xDatas: [
        {
          value: 20,
          datas: [
            { name: "纯新增", value: "41", unit: "人" },
            { name: "存量流失", value: "40", unit: "人" },
          ],
        },
        {
          value: 30,
          datas: [
            { name: "纯新增", value: "41", unit: "人" },
            { name: "存量流失", value: "40", unit: "人" },
          ],
        },
        {
          value: 40,
          datas: [
            { name: "纯新增", value: "41", unit: "人" },
            { name: "存量流失", value: "40", unit: "up" },
          ],
        },
        {
          value: 40,
          datas: [
            { name: "纯新增", value: "41", unit: "人" },
            { name: "存量流失", value: "40", unit: "up" },
          ],
        },
        {
          value: 40,
          datas: [
            { name: "纯新增", value: "41", unit: "人" },
            { name: "存量流失", value: "40", unit: "up" },
          ],
        },
        {
          value: 60,
          datas: [
            { name: "纯新增", value: "41", unit: "人" },
            { name: "存量流失", value: "40", unit: "up" },
          ],
        },
      ],
      xName: ["全行", "重点区域", "六行", "京津翼", "长三角", "粤港澳"],
      title: "标题",
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
