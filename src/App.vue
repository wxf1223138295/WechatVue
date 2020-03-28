<template>
  <div id="app">
    <router-view></router-view>
    <tab-bar>
      <tab-bar-item-left path="/home">
        <img
          style="height:90%"
          slot="item-icon"
          src="./assets/img/iconfont/hospital_info.png"
          alt=""
        />
        <img
          style="height:90%"
          slot="item-icon-active"
          src="./assets/img/iconfont/hospital_info_active.png"
          alt=""
        />
        <div slot="item-text">医院信息</div>
      </tab-bar-item-left>
      <tab-bar-item path="/shopcart">
        <img
          style="height:100%"
          slot="item-icon"
          src="./assets/img/iconfont/hospital_server.png"
          alt=""
        />
        <img
          style="height:100%"
          slot="item-icon-active"
          src="./assets/img/iconfont/hospital_server_active.png"
          alt=""
        />
        <div slot="item-text">医院服务</div>
      </tab-bar-item>
      <tab-bar-item-right path="/profile">
        <img
          style="height:90%"
          slot="item-icon"
          src="./assets/img/iconfont/my_info.png"
          alt=""
        />
        <img
          style="height:90%"
          slot="item-icon-active"
          src="./assets/img/iconfont/my_info_active.png"
          alt=""
        />
        <div slot="item-text">我的</div>
      </tab-bar-item-right>
    </tab-bar>
  </div>
</template>
<script>
import TabBar from "./components/tabbar/tabbar";
import TabBarItem from "./components/tabbar/tabbarItem";
import TabBarItemLeft from "./components/tabbar/tabbarItem_left";
import TabBarItemRight from "./components/tabbar/tabbarItem_right";

export default {
  name: "App",
  components: {
    TabBar,
    TabBarItem,
    TabBarItemLeft,
    TabBarItemRight
  }
};
</script>
<style>
@import "./assets/css/base.css";
.active {
  color: blue;
}
</style>
