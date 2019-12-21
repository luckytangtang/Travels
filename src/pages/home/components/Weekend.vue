<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="border-bottom" v-for="item of recommendList" :key="item.id">
       <div class="item-img-wrapper">
         <img  class="item-img" :src=item.imgUrl>
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
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/df3482c04dfdeba340e588d9ca97bb88.jpg_600x330_b0da71bb.jpg',
          title: '岳麓书院',
          desc: '最具文化历史底蕴的书屋，感受千年的文化熏陶'
        }, {
          id: '0002',
          imgUrl: '//img1.qunarzz.com/sight/p0/1412/68/42da26a54c27a3c237b4d10a61583c36.water.jpg_600x330_bd7fbe7f.jpg',
          title: '长沙圣地海洋公园',
          desc: '浪漫的长沙首站，浪漫的海洋主题公园'
        }, {
          id: '0003',
          imgUrl: '//img1.qunarzz.com/sight/p0/1505/57/579b6c97900745db.water.jpg_600x330_a7a104d2.jpg',
          title: '橘子洲',
          desc: '独立寒秋，湘江北去，橘子洲头，数风流人数，还看今朝'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .title
    margin-top :.1rem    //距离上一层的页距
    line-height:.5rem   //行高
    background :#eee
    text-indent :.5rem  //第一行的缩进
  .item-img-wrapper
    overflow :hidden    //该元素的内容若超出了给定的宽度和高度属性,那么超出的部分将会被隐藏
    margin-top :.1rem
    height :0
    padding-bottom :38%  // 如果用%来表示的话,计算是根据父元素的width的值进行计算的 width * 比例
    .item-img
      width: 100%
  .item-info
    padding:.1rem
    .item-title
      line-height :.54rem
      font-size :.32rem
      ellipsis()
    .item-desc
      line-height :.4rem
      color: #ccc
      ellipsis()

</style>
