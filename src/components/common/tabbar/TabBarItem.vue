<template>
  <div class="tab-bar-item" @click="itemClick">
    <!-- 具名插槽 用来验证动态替换的元素 -->
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :class="{active:isActive}"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name:'TabBarItem',
  props:{
    path:String
  },
  data() {
    return {}
  },
  computed:{
    isActive(){
      // 判断当前活跃路由 是否与 当前路由一致
      return this.$route.path.indexOf(this.path) !== -1
    }
  },
  methods: {
    itemClick(){
      // 防止重复点击路由报错 ，需要把router的三个参数补齐
      this.$router.replace(this.path,()=>{},err=>err)
    }
  },
}
</script>

<style>
 .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
  }
  .tab-bar-item img {
    width: 24px;
    height: 24px;
  }
  .active {
    color: #73b4ff;
  }
</style>