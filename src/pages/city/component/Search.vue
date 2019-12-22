<template>
  <div>
    <div class="search">
      <input  class="search-input" type="text" placeholder="请输入城市名或者拼音">
    </div>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
.search
  background :$bgcolor
  height :.72rem
  padding:0.1rem
  .search-input
    box-sizing: border-box
    width :100%
    height :.62rem
    padding:0.1rem
    line-height: .62rem
    text-align: center
    border-radius: .06rem  //给元素设置圆角边框
    color: #666
</style>
