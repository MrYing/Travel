<template>
    <div class="content-weekend">
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item"
            v-for="item of weekendList"
            :key="item.id">
              <div class="item-img-wrapper">
                    <img class="item-img" :src='item.imgUrl'/>
              </div>
                <div class="item-info">
                    <p class="item-title" v-text="item.title"></p>
                    <p class="item-desc" v-text="item.desc"></p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      weekendList: [{
        id: '01',
        title: '南京必游TOP10',
        desc: '看尽王侯将相荣辱成败，六朝金粉潮起潮落',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg'
      },
      {
        id: '02',
        title: '民国情怀国共风华',
        desc: '找到你心中想要的那个民国时期的南京',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/e1/cdbf56d837da59.jpg_r_640x214_105fc3f2.jpg'
      }, {
        id: '03',
        title: '孩子的游玩地',
        desc: '让小朋友们欢脱起来',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ed/8bce72632c9136.jpg_r_640x214_221c04c6.jpg'
      },
      {
        id: '04',
        title: '长江烂漫景',
        desc: '览滚滚长江，看山花烂漫',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/ff/19b65f7ca38d70.jpg_r_640x214_c9a4a14b.jpg'
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
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()

</style>
