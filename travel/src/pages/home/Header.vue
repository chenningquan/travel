<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe743;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe61e;</span>
      输入景点/城市/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont city-icon">&#xe752;</span>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        font-size .5rem
        text-align center
    .header-input
      flex 1
      height .64rem
      line-height .64rem
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      background white
      border-radius .1rem
      color #ccc
    .header-right
      min-width 1.04rem
      padding 0 .1rem
      float right
      text-align center
      color #ffffff
      .city-icon
        margin-left -.04rem
        font-size .3rem
</style>
