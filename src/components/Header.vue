<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{ this.city }}
      <span class="iconfont">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '../assets/styles/varibles.styl'
.header
  display flex
  line-height .86rem
  background-color #00bcd4
  color #fff
  .header-left
    width .64rem
    float left
    text-align center
  .header-input
    flex 1
    height .64rem
    line-height .64rem
    margin-top .12rem
    margin-left .2rem
    padding-left .2rem
    background-color #fff
    border-radius .1rem
    color #ccc
  .header-right
    width 1.24rem
    float right
    text-align center
</style>
