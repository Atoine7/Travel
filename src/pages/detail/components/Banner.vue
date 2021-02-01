<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//imgs.qunarzz.com/p/p67/1512/a2/0ebfcd965b9391f7.jpg_256x160_04d5813d.jpg" alt="banner">
      <div class="banner-info">
        <div class="banner-title">
          大连圣亚海洋世界（AAAA景区）
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe667;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      @close="handleGallaryClose"
      v-show="showGallary"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'

export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=2872791927,4075468899&fm=26&gp=0.jpg',
        'https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=2872791927,4075468899&fm=26&gp=0.jpg']
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
    CommonGallary
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
    background-image: linear-gradient(top, rgba(0, 0, 0, 0),rgba(0, 0, 0, 0.8))
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
