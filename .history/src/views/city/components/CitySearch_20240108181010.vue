<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="Enter city name" />
  </div>
</template>

<script lang="ts">
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/varibles.styl'
.search
  height: .72rem
  padding: 0 .1rem
  background: $bgColor
  .search-input
    box-sizing: border-box
    width: 100%
    height: .62rem
    padding: 0 .1rem
    line-height: .62rem
    text-align: center
    border-radius: .06rem
    color: #666
</style>
