<template>
  <div class="navbar">
    <div class="left"> <slot name="left"></slot></div>
    <div class="center"> <slot name="center"></slot></div>
    <div class="right"> <slot name="right"></slot></div>
  </div>
</template>

<script>
export default {
  name:"NavBar"
}
</script>

<style>
  .navbar{
    display: flex;
    line-height: 44px;
    height: 40px;
    text-align: center;
    /* 不要在这里设置背景颜色，一旦设置就被定死，其他页面也会使用同样的背景颜色 */
    /* background-color: pink;  */
    box-shadow: 0 1px 1px rgba(100, 100, 100, .1);
  }
  .left,.right{
    width: 60px;
  }
  .center{
    flex: 1;
  }
</style>