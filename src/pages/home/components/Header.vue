<template>
  <div class="header">
    <div class="header-left">
      <i class="iconfont icon--left-arrow"></i>
    </div>
    <div class="header-middle">
      <div class="kw">
        <i class="iconfont icon-fangdajing search-icon"></i>
        输入城市/景点/游玩主题
      </div>
      <input type="text" class="header-input"/>
    </div>
    <div class="header-right">
      城市
      <i class="iconfont icon-xiajiantou"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl'
.header {
  display: flex;
  background-color: $bgColor;
  height: .88rem;
  color: #fff;
  line-height: .88rem;
}
.header .header-left {
  width: .8rem;
  height: 100%;
  text-align: center;
}
.header .header-right {
  width: 1.32rem;
  height: 100%;
  text-align: center;
}
.header .header-middle {
  position: relative;
  flex: 1;
}
.header .header-middle .kw{
  position: absolute;
  left: .1rem;
  color: #e4e7ea;
}
.header .header-middle .header-input{
  width: 100%;
  height: 66%;
  border-radius: 0.06rem;
}
</style>
