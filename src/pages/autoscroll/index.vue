<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-look_box
          auto-scroll(:tables='tables', :option='option')
            .demo-table
              .demo-table_item(v-for='item in tables')
                .item-name {{ item.name }}
                .item-age {{ item.age }}
                .item-sex {{ item.sex }}
                .item-love {{ item.love }}
      .page-coder
        .page-coder_title 使用
        .page-coder_content {{ htmlData }}
          
    .page-control
      .page-control_title 参数详解
      .page-control_content
        p 
          b 注意：
          | 父级容器确定大小

        p 
          b tables: {{ tables }}，
          | 滚动的tables列表
        .page-control_control
          
      
        p 
          b option: {{ option }}，
          | 滚动配置项, 可传可不传，默认配置如下
        .page-control_control.c-c
        
</template>
<script>
export default {
  name: "yq-percentage",
  data() {
    return {
      htmlData: `<auto-scroll :tables='tables' :option="option">自定义列表</auto-scroll>`,
      tables: [
        { name: "yq", age: 18, sex: "man", love: "game" },
        { name: "yq", age: 18, sex: "man", love: "game" },
        { name: "yq", age: 18, sex: "man", love: "game" },
        { name: "yq", age: 18, sex: "man", love: "game" },
        { name: "yq", age: 18, sex: "man", love: "game" },
        { name: "yq", age: 18, sex: "man", love: "game" },
        { name: "yq", age: 18, sex: "man", love: "game" },
      ],
      option: {},
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
