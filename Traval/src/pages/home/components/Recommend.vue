<template>
  <div>
    <div class="title"><span class="iconfont">&#xe85c;</span>猜你喜欢</div>
    <ul>
      <li class="item" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
        title: '深圳野生动物园',
        desc: '深圳市野生动物园有限公司是中国第一家放养式的野生动物园',
        address: '南山区'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1911/6c/6c31c4988aade7aba3.water.jpg_200x200_fe5c186f.jpg',
        title: '深圳欢乐谷',
        desc: '深圳欢乐谷是华侨城集团新一代大型主题乐园，首批国家AAAAA级旅游景区，占地面积35万平方米，总投资20亿元人民币，是 一座融参与性、观赏性、娱乐性、趣味性于一体的中国现代主题乐园。',
        address: '南山区'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/f2/f2e0213052717f7ca3.water.jpg_200x200_816c1b48.jpg',
        title: '世界之窗',
        desc: '世界之窗是香港中旅国际投资有限公司控股、华侨城集团参股的旅游项目。',
        address: '华侨城'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201301/16/4593d3d5a27f445b93835fbb.jpg_200x200_2fcb6c78.jpg',
        title: '东部华侨城大侠谷',
        desc: '大侠谷生态乐园（又名“大峡谷”）位于深圳东部华侨城，俯瞰深圳东部黄金海岸线，集山地郊野公园和都市主题公园于一体',
        address: '东部华侨城'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/9d/9d8c0e9a01bba92e90.water.jpg_200x200_86f2e623.jpg',
        title: '锦绣中华民俗村',
        desc: '锦绣中华和中国民俗文化村是深圳锦绣中华发展有限公司辖下的两大景区',
        address: '华侨城'
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
