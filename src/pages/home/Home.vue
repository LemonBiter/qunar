<template>
  <div>
    <my-home-header></my-home-header>
    <home-swiper></home-swiper>
    <div>{{ msg }}</div>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
export default {
  name: 'Home',
  components: {
    MyHomeHeader: HomeHeader,
    HomeSwiper
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
