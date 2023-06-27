<template>
  <MainHeader/>
  <div class="content">
    <MainProfile></MainProfile>
    <StatProfile></StatProfile>
    <SoftwareProfile></SoftwareProfile>
  </div>
</template>

<script>
import MainProfile from './components/MainProfile.vue'
import MainHeader from './components/MainHeader.vue'
import StatProfile from './components/StatProfile.vue'
import SoftwareProfile from './components/SoftwareProfile.vue'

export default {
  name: 'App',
  components: {
    MainProfile,
    MainHeader,
    StatProfile,
    SoftwareProfile,
  }
}
</script>

<style lang="scss">

.content {
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

* {
  color: $secondary-color;
  margin: 0;
  padding: 0;
  font-family: "Open Sans",Helvetica,sans-serif;
  font-weight: 400;
}

body {
}

html {
}

a {
  text-decoration: none;
}

@media only screen and (min-width: 1200px) {
  html {
    scroll-snap-type: y mandatory;
  }
}
</style>
