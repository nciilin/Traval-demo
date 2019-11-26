<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>

import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '成人票',
        price: '228.9'
      }, {
        title: '学生票',
        price: '190'
      }, {
        title: '儿童票',
        price: '140'
      }, {
        title: '亲子票',
        price: '339.1'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .content
    height: 50rem
</style>
