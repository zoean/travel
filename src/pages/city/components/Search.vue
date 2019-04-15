<template>
<<<<<<< HEAD
<div>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音" name="">
  </div>
  <div class="search-content">
    <ul>
      <li>123</li>
    </ul>
  </div>
=======
<div class="search">
  <input v-model="keyword" class="search-input" type="text" placeholder="输入城市名或拼音" name="">
>>>>>>> city-search-logic
</div>
</template>

<script>
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.spell.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  }
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
