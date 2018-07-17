<template>
  <div>
    <div class="title">
      热销推荐
    </div>
    <ul>

        <router-link tag="li"
                     class="item border-bottom"
                     v-for="item of list"
                     :to="'/detail/'+item.id"
        >
          <img class="item-img" :src="item.imgUrl" alt="">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </router-link>

    </ul>
  </div>
</template>

<script>
    export default {
        name: "HomeRecommend",
        props:{
          list:Array
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
  .item
    display flex
    height 2.1rem
    overflow hidden

    .item-img
      width 2rem
      padding .1rem
    .item-info
      flex:1
      padding .1rem
      min-width 0
      .item-title
        line-height .6rem
        font-size .36rem
        ellipsis()
      .item-desc
        line-height .5rem
        color #ccc
        ellipsis()
      .item-button
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        margin-top .2rem
        line-height .44rem

</style>
