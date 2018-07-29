<template>
    <div class="content-recommend">
        <div class="title">热销推荐</div>
        <ul v-for="item of recommendList" :key="item.id">
            <li class="item">
                <div class="item-img">
                    <img class="img-url" :src='item.imgUrl'/>
                </div>
                <div class="item-info">
                    <p class="item-title" v-text="item.title"></p>
                    <p class="item-desc" v-text="item.desc"></p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default{
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '01',
        title: '南京欢乐水魔方',
        desc: '五颗星魔幻广场 1543条评论',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/03b24acde057acb03c1b514bd2bf638c.jpg_200x200_00cebaa5.jpg'
      },
      {
        id: '02',
        title: '南京海底世界',
        desc: '五颗星魔幻广场 1543条评论',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/13/0cd5a9a57ae0d1b9b935ec604ce0f9bf.water.jpg_200x200_9b808f51.jpg'
      }, {
        id: '03',
        title: '南京总统府',
        desc: '五颗星魔幻广场 1543条评论',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/f7/f7c3be996152011c.img.jpg_200x200_0b707f70.jpg'
      }, {
        id: '04',
        title: '红山动物园-动物王国',
        desc: '五颗星魔幻广场 1543条评论',
        imgUrl: 'http://img1.qunarzz.com/sight/201312/03/38da27f8a2ad319ec8d65eac.jpg_200x200_72a1d26d.jpg'
      }, {
        id: '05',
        title: '南京中国科举博物馆（江南贡院）',
        desc: '五颗星魔幻广场 1543条评论',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/c0/c01ae3666c4d4043.img.jpg_200x200_511a3866.jpg'
      }

      ]
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
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      overflow hidden
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .2rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
