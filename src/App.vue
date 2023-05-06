<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
  }
}
</script>

<template>
  <Header/>
  <Jumbotron/>
  <Main/>
</template>

<style lang="scss">
@use './scss/main.scss' as *;
</style>