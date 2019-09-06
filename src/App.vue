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
        // Twitter Card
        {name: 'twitter:card', content: 'summary'},
        {name: 'twitter:title', content: 'Vue Social Cards Example'},
        {name: 'twitter:description', content: 'Vue sample site showing off Twitter and Facebook Cards.'},
        {name: 'twitter:image', content: this.logo},

        // Facebook OpenGraph
        {property: 'og:title', content: 'Vue Social Cards Example'},
        {property: 'og:site_name', content: 'Vue Example'},
        {property: 'og:type', content: 'website'},
        {property: 'og:image', content:  this.logo},
        {property: 'og:description', content: 'Vue sample site showing off Twitter and Facebook Cards.'}
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
