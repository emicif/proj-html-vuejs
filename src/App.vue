<template>
  <div id="app">
    <HeaderComponent />
    <MainComponent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'




export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
   max-width: 1200px;
   margin: 0px auto;
}
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}

// utilities
.flex {
  display: flex;
}
</style>
