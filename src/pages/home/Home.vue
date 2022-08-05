<template>
  <div>
    <my-home-header></my-home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <div>{{ msg }}</div>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
export default {
  name: 'Home',
  components: {
    MyHomeHeader: HomeHeader,
    HomeSwiper,
    HomeIcons
  },
  data () {
    return {
      msg: 'home'
    }
  }
}
</script>

<style scoped>

</style>
