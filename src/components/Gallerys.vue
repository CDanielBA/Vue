<script setup >
    // Import Swiper Vue.js components
    import {Navigation, Pagination, A11y, Virtual} from 'swiper'
    import { Swiper, SwiperSlide } from 'swiper/vue';
  
    // Import Swiper styles
    import 'swiper/css';
    import 'swiper/css/navigation';
    import 'swiper/css/pagination';

</script>

<template>
  <swiper
    :slides-per-view="1"
    :space-between="50"
    :modules="[Navigation,Pagination,A11y,Virtual]" navigation
    :pagination="{clickable:true, dynamicBullets:true}" grab-cursor virtual
  >
    <swiper-slide v-for = "n in 10" :key="n" :virtualIndex="n" >
      <img :src="'https://picsum.photos/1024/600?random='+n" alt="">
    </swiper-slide>
    
  </swiper>
</template>
<style>
.swiper{
  width: 800px;
}
@media (max-width: 1000px) {
  .swiper{
    width: 400px;
    height: 200px;
    margin-bottom: 20px;
  }
}
@media(max-width:620px){
  .swiper{
    width: 320px;
    height: 200px;
    margin-bottom: 20px;
  }
}
</style>
