<template>
<div>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音" name="">
  </div>
  <div class="search-content">
    <ul>
      <li>123</li>
    </ul>
  </div>
</div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.search
  height: .72rem
  background: $bgColor
  padding: 0 .1rem
  .search-input
    width: 100%
    height: .62rem
    line-height: .62rem
    text-align: center
    border-radius: .06rem
    padding: 0 .1rem
    box-sizing: border-box
.search-content
  position: absolute
  top: 1.58rem
  left: 0
  right: 0
  bottom: 0
  background: green
  z-index: 1
</style>
