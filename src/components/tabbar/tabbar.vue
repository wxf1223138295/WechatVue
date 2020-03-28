<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: "TabBar"
};
</script>
<style>
@import "../../assets/css/base.css";
#tab-bar {
  display: flex;
  position: fixed;
  background-image: url(../../assets/img/iconfont/button_img.png);
  background-size: cover;
  background-position: center;
}
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
}
</style>
