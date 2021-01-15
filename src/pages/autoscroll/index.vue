<template lang="pug">
  .page-wrapper
    .page-header
      .page-look
        .page-look_title 视图
        .page-look_box
          auto-scroll(:tables='tables', :option='option')
            .demo-table
              .demo-table_item(v-for='item in tables')
                .item.item-name {{ item.name }}
                .item.item-age {{ item.age }}
                .item.item-sex {{ item.sex }}
                .item.item-love {{ item.love }}
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
          b 1、tables：
          | 滚动的tables数组
        .page-control_control
          
      
        p 
          b 2、option: {{ option }}，
          | 滚动配置项, 可传可不传，默认配置例。
        .page-control_control
        p 1、step：数值越大速度滚动越快。
        p 2、limitMoveNum：开启无缝滚动的数据量
        p 3、hoverStop：是否启用鼠标hover控制
        p 4、direction：方向 0 往下 1 往上 2向左 3向右
        p 5、openTouch：移动端开启touch滑动
        p 6、singleHeight：单步运动停止的高度(默认值0是无缝不停止的滚动) direction => 0/1
        p 7、singleWidth：单步运动停止的宽度(默认值0是无缝不停止的滚动) direction => 2/3
        p 8、waitTime：单步停止等待时间(默认值1000ms)
        p 9、switchOffset：左右切换按钮距离左右边界的边距(px)
        p 10、autoPlay：1.1.17版本前手动切换时候需要置为false
        p 11、switchSingleStep：手动单步切换step值(px)
        p 12、switchDelay：单步切换的动画时间(ms)
        p 13、switchDisabledClass：不可以点击状态的switch按钮父元素的类名
        p 14、isSingleRemUnit：singleHeight and singleWidth是否开启rem度量


        
</template>
<script>
export default {
  name: "yq-autoscroll",
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
      option: {
        step: 0.8, // 数值越大速度滚动越快
        limitMoveNum: 5, // 开启无缝滚动的数据量
        hoverStop: true, // 是否启用鼠标hover控制
        direction: 1, // 方向 0 往下 1 往上 2向左 3向右
        openTouch: false, // 移动端开启touch滑动
        singleHeight: 0, // 单步运动停止的高度(默认值0是无缝不停止的滚动) direction => 0/1
        singleWidth: 0, // 单步运动停止的宽度(默认值0是无缝不停止的滚动) direction => 2/3
        waitTime: 1000, // 单步停止等待时间(默认值1000ms)
        switchOffset: 30, // 左右切换按钮距离左右边界的边距(px)
        autoPlay: true, // 1.1.17版本前手动切换时候需要置为false
        switchSingleStep: 134, // 手动单步切换step值(px)
        switchDelay: 400, // 单步切换的动画时间(ms)
        switchDisabledClass: "disabled", // 不可以点击状态的switch按钮父元素的类名
        isSingleRemUnit: false, // singleHeight and singleWidth是否开启rem度量
      },
    };
  },
};
</script>
<style lang="scss">
@import "./index.scss";
</style>
