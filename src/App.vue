<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import'~bootstrap/scss/bootstrap';
@import "./style/variables.scss";

.h6_style {
      font-weight: bold;
      text-transform: uppercase;
    }

.tag_btn {
    height: 20px;
    width: 80px;
    line-height: 20px;
    background-color: $blackColor;
    color: $whiteColor;
    text-transform: uppercase;
    font-size: 10px;
    margin-left: 5px;
    border-radius: 5px;
}
/*
#app {
  background-color: white;
}
*/
</style>
