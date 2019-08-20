<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1604/1e/1e75f8e1af9fe81f90.img.jpg_600x330_aeba2c96.jpg" />
      <div class="banner-info">
        <div class="banner-title">世界花卉大观园(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe643;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data(){
    return {
      showGallary: false,
      imgs: ["http://img1.qunarzz.com/sight/p55/201211/04/fbcab3e5d6479ce893835fbb.jpg_r_800x800_6360f514.jpg", "http://img1.qunarzz.com/sight/p0/1410/e3/73da8d3e19cdc41c1932d4fcd22ec792.water.jpg_r_800x800_7f96ccf9.jpg"]
    }
  },
  methods: {
    handleBannerClick(){
      this.showGallary = true
    },
    handleGallaryClose(){

      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
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
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    line-height: .6rem
    color: #fff
    .banner-title
      flex: 1
      font-size: .32rem
      padding: 0 .2rem
    .banner-number
      margin-top: .14rem
      padding: 0 .4rem
      line-height: .32rem
      height: .32rem
      border-radius: .2rem
      font-size: .24rem
      background: rgba(0, 0, 0, .8)
      .banner-icon
        font-size: .24rem
        margin-right: .06rem
</style>
