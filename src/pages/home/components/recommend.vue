<template>
  <div>
    <div class='title'>热销推荐</div>
    <ul>
      <li
        class='item border-bottom'
        v-for='item of recommendList'
        :key='item.id'
      >
        <img class='item-img' :src='item.imgUrl' />
        <div class='item-info'>
          <p class='item-title'>{{ item.title }}</p>
          <p class='item-desc'>{{ item.desc }}</p>
          <button class='item-button'>查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            '//img1.qunarzz.com/sight/p0/1605/58/5847560fd55ff6f590.water.jpg_256x160_13631f57.jpg',
          title: '凤凰古城',
          desc: '邂逅数个人，偶遇一座城'
        },
        {
          id: '0002',
          imgUrl:
            '//img1.qunarzz.com/sight/p0/2011/1b/1b5e5d4a4003bbc3a3.img.jpg_256x160_2448993c.jpg',
          title: '张家界国家森林公园',
          desc: '三千奇峰，八百秀水'
        },
        {
          id: '0003',
          imgUrl:
            '//img1.qunarzz.com/sight/p0/1412/e2/650fc27b271e57e2b8ea952aa3e48eea.water.jpg_256x160_45707f83.jpg',
          title: '衡山风景区',
          desc: '华山如立，嵩山如卧，惟有南岳衡山独如飞'
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
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
