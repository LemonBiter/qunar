<template>
  <div>
    <div>{{ msg }}</div>
    <router-link to="/list">列表页</router-link>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'home'
    }
  }
}
</script>

<style scoped>

</style>
