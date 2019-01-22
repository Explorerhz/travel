<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="item in imgList" :key="item.id">
        <img class="swiper-img" :src="item.img" alt="">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      },
      imgList: [
        {
          id: '001',
          img: 'http://img1.qunarzz.com/piao/fusion/1812/d6/daa880b254940402.jpg_750x200_b114308a.jpg'
        },
        {
          id: '002',
          img: 'http://img1.qunarzz.com/piao/fusion/1811/31/da037478f37cf202.jpg_750x200_fe28d396.jpg'
        }
      ]
    }
  },
  mounted () {
  }
}
</script>
<style lang='stylus' scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 26.67%;
    background-color: #eeeeee
    .swiper-img
      width: 100%;
</style>
