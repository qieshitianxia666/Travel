<template>
  <div>
    <div class="title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: "HomeRecommend",
        data(){
          return{
            recommendList:[{
              id:'0001',
              imgUrl:'http://img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_200x200_36727f69.jpg',
              title:'金海湖风景区',
              desc:'金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区'
            },{
              id:'0002',
              imgUrl:'http://img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_200x200_36727f69.jpg',
              title:'金海湖风景区',
              desc:'金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区'
            },{
              id:'0003',
              imgUrl:'http://img1.qunarzz.com/sight/p0/1609/7a/7ae8ee7831836095a3.water.jpg_200x200_36727f69.jpg',
              title:'金海湖风景区',
              desc:'金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区金海湖风景区'
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
