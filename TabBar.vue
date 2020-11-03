<template>
  <div id="tabbar">
    <tab-bar-item path="/home">
      <img slot="item-icon" src="~assets/img/home.svg" alt="" />
      <img slot="item-icon-active" src="~assets/img/home_active.svg" alt="" />
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path='/category'>
      <img slot="item-icon" src="~assets/img/category.svg" alt="" />
      <img slot="item-icon-active" src="~assets/img/category_active.svg" alt="" />
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item  path='/shopcart'>
      <img slot="item-icon" src="~assets/img/shopcart.svg" alt="" />
      <img slot="item-icon-active" src="~assets/img/shopcart_active.svg" alt="" />
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item  path='/profile'>
      <img slot="item-icon" src="~assets/img/profile.svg" alt="" />
      <img slot="item-icon-active" src="~assets/img/profile_active.svg" alt="" />
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </div>
</template>

<script>
import TabBarItem from "./TabBarItem";

export default {
  name: "tabbar",
  components: {
    TabBarItem,
  },
};
</script>

<style>
#tabbar {
  display: flex;
  background-color: #f6f6f6;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  box-shadow: 0 -2px 1px rgba(100, 100, 100, 0.1);
}
</style>