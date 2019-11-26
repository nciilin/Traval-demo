<template>
  <div>
    <div class="wrapper">
      <div class="ticket border-bottom">
        <span class="ticket-type"></span>日场夜场通用
      </div>
      <div
        class="item clearfix"
        v-for="( item, index ) of list"
        :key="index"
      >
        <div class="item-title border-bottom">
          {{item.title}}
          <div class="item-price">{{'￥' + item.price}}
            <span class="start-price">起</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  .clearfix::after
    content: ''
    display: block
    clear: both
  .wrapper
    margin-bottom: .2rem;
    .ticket
      overflow: hidden
      position: relative
      z-index: 4
      margin-bottom: -.02rem
      padding: 0 .2rem
      height: .88rem
      background: #fff
      color: #333
      font-size: .32rem
      line-height: .88rem
      text-indent: .4rem
      .ticket-type
        display: inline-block
        position: absolute
        width: .36rem
        height: .36rem
        top: .26rem
        left: .2rem
        background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
        margin-right: .1rem
        background-size: .4rem 3rem
    .item
      .item-title
        line-height: .8rem
        font-size: .32rem
        padding: 0 .2rem
      .item-price
        float: right
        color: #ff9800
        .start-price
          font-size: .06rem
</style>
