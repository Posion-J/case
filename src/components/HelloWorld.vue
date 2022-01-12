<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide">揪子</div>
      <div class="swiper-slide">揪子</div>
      <div class="swiper-slide">揪子</div>
    </div>
    <!-- 如果需要分页器 -->
    <div class="swiper-pagination"></div>
    <!-- 如果需要导航按钮 -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
    <!-- 如果需要滚动条 -->
    <div class="swiper-scrollbar"></div>
  </div>
</template>

<script>
import Swiper from 'swiper';
import 'swiper/dist/css/swiper.min.css';
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted(){
    /* eslint-disable no-new */
    new Swiper('.swiper-container', {
      loop:true,
      autoplay:true,
      speed: 3000,
      pagination: {
        el: '.swiper-pagination',
      },
    })
  }

  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.swiper-container {
  width: 600px;
  height: 300px;
}
.swiper-slide:nth-child(even){
  background: greenyellow;
}
.swiper-slide:nth-child(odd){
  background: yellow;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
