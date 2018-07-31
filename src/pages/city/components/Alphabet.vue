<template>
  <ul class="list">
    <li
      class="item"
      v-for="(item, key) of cities"
      :key="key"
    >
      {{key}}
    </li>
  </ul>
</template>
<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.list
    position :absolute;
    top :80px
    right :0
    bottom:0
    width: 20px
    display flex
    flex-direction :column
    justify-content center
    li
        text-align :center
        padding: 3px;
        color :$bgColor
</style>
