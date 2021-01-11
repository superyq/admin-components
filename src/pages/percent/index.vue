<template>
  <div class="percentage-box">
    <c-percentage
      width="70%"
      :background="['#002adb', '#04f7fb']"
      :haveBg="false"
      rem
    ></c-percentage>
  </div>
</template>
<script>
export default {
  name: "yq-percentage",
};
</script>
<style lang="scss">
.percentage-box {
  width: 100px;
  height: 20px;
}
</style>
