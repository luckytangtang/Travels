<template>
  <ul class="list">
   <li class="item" v-for="(item,key) of cities" :key="key">
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
@import "~styles/varibles.styl"
.list
  display: flex      //弹性布局
  flex-direction: column  //主轴为垂直方向
  justify-content: center  //居中对齐
  position: absolute
  top: 1.58rem
  right: 0
  bottom: 0
  width: .4rem
  .item
    line-height: .4rem
    text-align: center
    color: $bgcolor
</style>
