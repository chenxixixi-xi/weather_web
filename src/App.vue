<template>
  <div id="app">
    <HelloWorld msg="Weather data  "/>
    <!-- <a :href="'https://api.caiyunapp.com/v2/place?token=VKC3aGqblsPQTRQT&lang=en_US&query=s'">Get latitude and longitude;    </a>
    <a :href="'https://api.caiyunapp.com/v2.5/VKC3aGqblsPQTRQT/-69.86667,18.49333/realtime.json?lang=en_US'">Get weather data based on latitude and longitude </a> -->

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
