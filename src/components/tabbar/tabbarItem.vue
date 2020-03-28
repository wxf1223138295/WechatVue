<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: "blue"
    }
  },  
  data() {
    return {
      //   isActive: true
    };
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1;
    },
    activeStyle() {
      return this.isActive ? { color: this.activeColor } : {};
    }
  },
  methods: {
    itemClick() {
      if (!this.isActive) {
        this.$router.replace(this.path);
      }
    }
  }
};
</script>
<style>
@import "../../assets/css/base.css";
#tab-bar {
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  height: 90;
}
.tab-bar-item {
  flex: 1;
  height: 49px;
  font-size: 12px;
  text-align: center;
  color: #808080;
}
.tab-bar-item img {
  width: 33px;
  height: 33px;
  margin-top: 15px;
  vertical-align: middle;
}
</style>
