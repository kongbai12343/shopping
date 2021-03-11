<template>
     <tab-bar>
      <tab-bar-item path="/home">
        <img slot="item-icon" src="../assets/img/TabBar/index.png" alt="">
        <img slot="item-icon-active" src="../assets/img/TabBar/index_active.png" alt="">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category">
        <img slot="item-icon" src="../assets/img/TabBar/category.png" alt="">
        <img slot="item-icon-active" src="../assets/img/TabBar/category_active.png" alt="">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/shopcar">
        <img slot="item-icon" src="../assets/img/TabBar/shopCar.png" alt="">
        <img slot="item-icon-active" src="../assets/img/TabBar/shopCar_active.png" alt="">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile">
        <img slot="item-icon" src="../assets/img/TabBar/profile.png" alt="">
        <img slot="item-icon-active" src="../assets/img/TabBar/profile_active.png" alt="">
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
</template>

<script>
import TabBar from './TabBar/TabBar'
import TabBarItem from './TabBar/TabBarItem.vue'
export default {
  name:'MainTabBar',
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style>

</style>