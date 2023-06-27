<template>
  <MainHeader/>
  <div class="content">
    <MainProfile></MainProfile>
    <StatProfile></StatProfile>
    <SoftwareProfile></SoftwareProfile>
  </div>
</template>

<script>
import MainProfile from '@/views/MainProfile.vue'
import MainHeader from '@/components/Header/MainHeader.vue'
import StatProfile from '@/views/StatProfile.vue'
import SoftwareProfile from '@/views/SoftwareProfile.vue'

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
