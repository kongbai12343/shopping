<template>
  <div class="recommend">
    <div v-for="item in recommend" :key="item.index" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div class="title">{{ item.title }}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name:'HomeRecommend',
  props:{
    recommend:{
      type:Array,
      default(){
        return []
      }
    }
  }
}
</script>

<style>
 .recommend{
   display: flex;
   width: 100%;
   text-align: center;
   padding: 10px 0 20px;
   font-size: 12px;
 }

 .recommend-item{
   flex: 1;
 }
.recommend-item img {
  width: 65px;
  height: 65px;
  margin-bottom: 5px;
}

</style>