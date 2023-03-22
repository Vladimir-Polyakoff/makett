<script>
import Header from '@/views/Header'
import Footer from '@/views/Footer'

export default {
  name: 'TheApp',

  components: {
    Header,
    Footer
  }
}
</script>

<template>
  <div id="app">
    <Header></Header>
    <router-view/>
    <Footer></Footer>
  </div>
</template>

<style lang="scss">
body {
  background: #E5E5E5;
  width: 100%;
  display: flex;
  justify-content: center;
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 1920px;
  width: 100%;
  background: #fabcb4bb
}

</style>
