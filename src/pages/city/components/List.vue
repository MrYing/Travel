<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div
            class="button-wrapper"
            v-for="item of hot"
            :key="item.id"
          >
            <div class="button">{{item.name}}</div>
          </div>
        </div>
      </div>
      <div
        class="area"
        v-for="(item, key) of cities"
        :key="key"
      >
        <div class="title border-topbottom">{{key}}</div>
        <div class="item-list">
          <div
            class="item border-bottom"
            v-for="innerItem of item"
            :key="innerItem.id"
          >
            {{innerItem.name}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    hot: Array,
    cities: Object,
    letter: String
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.border-topbottom
    &:before
        border-color:#ccc
    &:after
        border-color:#ccc
.border-bottom
    &:before
        border-color:#ccc
.list
    position absolute
    top:89px
    left :0
    right :0
    bottom:0
    overflow hidden
    .title
        line-height: 24px
        background :#eee
        padding-left :10px
        color :#666
        font-size :14px
    .button-list
        padding :5px 30px 5px 5px
        overflow :hidden
        .button-wrapper
            width: 33.33%
            float: left
            .button
                margin :5px
                padding :5px
                border-radius:3px;
                text-align :center
                border :1px solid #ccc
    .item-list
        .item
            line-height :38px
            padding-left :10px
</style>
