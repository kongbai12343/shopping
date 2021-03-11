<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name:'TabBar'
}
</script>

<style>
  #tab-bar {
    background-color: #f6f6f6;
    /* 开启flex布局 */
    display: flex;
    /* 固定定位到底部 */
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    /* 添加盒子阴影 */
    box-shadow: 0 3px 1px rgba(100, 100, 100, .5);
  }

</style>