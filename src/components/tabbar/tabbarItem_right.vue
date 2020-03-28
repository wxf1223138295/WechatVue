<template>
  <div class="tab-bar-item-right" @click="itemClick">
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "TabBarItemRight",
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
  top: 90%;
}
.tab-bar-item-right {
  flex: 1;
  height: 49px;
  font-size: 12px;
  text-align: center;
  color: #808080;
}
.tab-bar-item-right img {
  width: 24px;
  height: 24px;
  margin-top: 25px;
  vertical-align: middle;
}
</style>
