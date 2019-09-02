<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
let ROOT_PATH = 'https://vue-social-cards-sample.netlify.com'
export default {
  name: 'app',
  data() {
    return {
      logo: ROOT_PATH + require('./assets/logo.png')
    }
  },
  components: {
    HelloWorld
  },
  metaInfo() {
    return {
      meta: [
         {name: 'twitter:card', content: 'summary_large_image'},
         {name: 'twitter:title', content: 'Vue Social Cards Example'},
         {name: 'twitter:image', content: this.logo},       
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
