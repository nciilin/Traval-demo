<template>
  <div>
    <div>
      <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_600x330_28bda6b0.jpg" alt="深圳野生动物园">
        <div class="banner-info">
          <div class="banner-title">深圳野生动物园(AAAA景区)</div>
          <div class="banner-number"><span class="iconfont banner-icon">&#xe66c;</span>22</div>
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    >
    </common-gallary>
  </div>
</template>

<script>

import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1508/44/c8fb5daa16f5f99f8201f323426b3516.water.jpg_r_800x800_e7642201.jpg',
        'http://img1.qunarzz.com/sight/p0/1508/79/334ed37d1fa6d6bf9baa0c7296ce4084.water.jpg_r_800x800_9a0660af.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
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
      color: #fff
      line-height: .6rem
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8));
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
        background-color: rgba(0,0,0,.8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
