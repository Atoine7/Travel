<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class='swiper-img' :src="item.imgUrl"
             alt="banner">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>

</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//source.qunarzz.com/site/images/wns/20210124_qunar_dujia_banner_750x192_5.jpg'
      }, {
        id: '0002',
        imgUrl: '//source.qunarzz.com/site/images/wns/20210121_qunar_dujia_750x192_2.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: white !important

.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 25.6%
  background: #eee

  .swiper-img
    width: 100%
</style>
