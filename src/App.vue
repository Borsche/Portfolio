<template>
  <MainHeader/>
  <div class="content">
    <MainProfile></MainProfile>
  </div>
</template>

<script>
import MainProfile from './components/MainProfile.vue'
import MainHeader from './components/MainHeader.vue'

export default {
  name: 'App',
  components: {
    MainProfile,
    MainHeader
  }
}
</script>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

* {
  color: $secondary-color;
  margin: 0;
  padding: 0;
}


a {

}
</style>
