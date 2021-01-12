<template lang='pug'>
  .page-wrapper
    .page-header
      .page-look
        .page-loading_box
          c-loading(:loading='true')
      .page-control

    .page-coder
</template>
<script>
export default {
  name: 'yq-loading'
}
</script>
<style lang='scss'>
@import "./index.scss";
</style>