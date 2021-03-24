<template>
  <div class="home">
    <router-view />
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"></home-swiper>
    <home-recommend :recommend="recommend"></home-recommend>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
import HomeSwiper from './childComps/HomeSwiper'
import HomeRecommend from './childComps/HomeRecommend'
import {getHomeDatas} from 'network/home'
export default {
  name:'Home',
  components:{
    NavBar,
    HomeSwiper,
    HomeRecommend
  },
  data() {
    return {
      banners:[],
      recommend:[]
    }
  },
  created() {
    getHomeDatas().then(res=>{
      //这里的this指向这个组件实例
      this.banners = res.data.banner.list;
      this.recommend = res.data.recommend.list;
    })
  },
}
</script>

<style>
.home-nav {
  background-color: var(--color-tint);
  color: #fff;
}
</style>