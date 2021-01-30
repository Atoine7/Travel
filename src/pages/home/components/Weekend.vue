<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img"
               :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1812/4c/33ad31d025fef.jpg_r_640x214_7821b813.jpg',
        title: '重庆夜景大赏',
        desc: '享巴渝特色，赏两江风光，感受不一样的重庆夜景！'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1904/45/45480d5910fab083a3.img.jpg_200x200_0d06f646.jpg',
        title: '武隆仙女山国家森林公园',
        desc: '又一个仙女下凡调戏牧童的故事'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1904/45/45480d5910fab083a3.img.jpg_200x200_0d06f646.jpg',
        title: '武隆仙女山国家森林公园',
        desc: '又一个仙女下凡调戏牧童的故事'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top: .2rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem

.item-img-wrapper
  overflow: hidden
  height: 0
  padding-bottom: 33.4%

  .item-img
    width: 100%

.item-info
  padding: .1rem

  .item-title
    line-he  ight: .54rem
    font-size: .32rem
    ellipsis()

  .item-desc
    line-height: .4rem
    color: #ccc
    ellipsis()
</style>
