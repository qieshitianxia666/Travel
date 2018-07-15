<template>
  <div>
    <div class="title">
      周末去哪儿
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>

        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "HomeWeekend",
    data() {
      return {
        recommendList: [{
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
          title: '漂流勇进，烧烤露营',
          desc: '金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区'
        }, {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
          title: '漂流勇进，烧烤露营',
          desc: '金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区'
        }, {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
          title: '漂流勇进，烧烤露营',
          desc: '金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区'
        }]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    line-height .8rem
    background #eee
    text-indent .2rem
    margin-top .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%

  .item-info
    padding .1rem
    .item-title
      line-height .6rem
      font-size .36rem
      ellipsis()
    .item-desc
      line-height .5rem
      color #ccc
      ellipsis()


</style>
