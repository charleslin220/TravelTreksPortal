<template>
  <div>
    <div class="title">Best Selling Recommendations</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">view full</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import type { PropType } from 'vue'
interface IconsItem {
  id: string
  imgUrl: string
  desc: string,
  title: string
}
export default {
  name: 'HomeRecommend',
  props: {
    list: Array as PropType<IconsItem[]>,
    default: () => [] // Provide a default empty array
  },
  data() {
    return {}
  }
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/mixins.styl'
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
