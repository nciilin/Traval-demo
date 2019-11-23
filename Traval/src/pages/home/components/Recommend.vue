<template>
  <div>
    <div class="title"><span class="iconfont">&#xe85c;</span>猜你喜欢</div>
    <ul>
      <li class="item" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="项目图片">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <span class="iconfont item-like">&#xe658;&#xe658;&#xe658;&#xe658;&#xe658;</span>
          <p class="item-like-address">{{item.address}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    text-indent: .2rem
    padding: .12rem 0 .13rem 0;
    .iconfont
      color: red
  .item
    display: flex
    height: 1.9rem
    overflow: hidden
    .item-img
      width: 1.8rem
      height: 1.8rem
      padding: .1rem
    .item-info
      flex: 1
      position: relative
      padding: .22rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        font-size: .24rem
        color: #ccc
        ellipsis()
      .item-like
        line-height: .4rem
        color: yellow
      .item-like-address
        position: absolute
        right: 0
        bottom: 0
        margin-right: .24rem
</style>
