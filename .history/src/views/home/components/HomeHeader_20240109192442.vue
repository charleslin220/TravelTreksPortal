<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      Enter City/Landmark/Play Theme
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{ doubleCity }}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { useStore, mapState, mapGetters } from 'vuex'
export default defineComponent({
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters('doubleCity')
  },
  setup() {
    const store = useStore()
    return {
      store
    }
  }
})
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/varibles.styl';
.header
  display: flex
  line-height: .86rem
  background: $bgColor
  color: #fff
  .header-left
    width: .64rem
    float:left
    .back-icon
      text-align: center
      font-size: .4rem
  .header-input
    flex: 1
    height: .64rem
    line-height .64rem
    margin-top: .12rem
    margin-left: .2rem
    padding-left: .2rem
    background: #fff
    border-radius: .1rem
    color: #ccc
  .header-right
    min-width: 1.1rem
    padding:0 .1rem
    float:right
    text-align: center
    color: #fff
    .arrow-icon
      margin-left: -.04rem
      font-size: .24rem
</style>
