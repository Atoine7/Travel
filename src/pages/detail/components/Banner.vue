<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" alt="banner">
      <div class="banner-info">
        <div class="banner-title">
          {{ sightName }}
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe667;</span>
          {{this.bannerImgs.length}}
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallary
        :imgs="bannerImgs"
        @close="handleGallaryClose"
        v-show="showGallary"
      ></common-gallary>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
  },
  data () {
    return {
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
  }
}
</script>

<style lang="stylus" scoped>
@font-face
  font-family: 'iconfont';
  src: url('//at.alicdn.com/t/font_2355112_838mauwdxs.eot');
  src: url('//at.alicdn.com/t/font_2355112_838mauwdxs.eot?#iefix') format('embedded-opentype'),
    url('//at.alicdn.com/t/font_2355112_838mauwdxs.woff2') format('woff2'),
    url('//at.alicdn.com/t/font_2355112_838mauwdxs.woff') format('woff'),
    url('//at.alicdn.com/t/font_2355112_838mauwdxs.ttf') format('truetype'),
    url('//at.alicdn.com/t/font_2355112_838mauwdxs.svg#iconfont') format('svg');
.banner
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 55%
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: .6rem
    color: #fff
    background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0),rgba(0, 0, 0, 0.8))
    .banner-title
      flex: 1
      font-size: .32rem
      padding: 0 .2rem
    .banner-number
      height: .32rem
      line-height: .32rem
      margin-top: .14rem
      padding: 0 .4rem
      border-radius: .2rem
      background: rgba(0, 0, 0, .8)
      font-size: .24rem
      .banner-icon
        font-size: .24rem
</style>
