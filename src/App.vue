<template>
  <div id="app">
    <Header :links="links"/>
    <Main/>
    <Footer :links="links"/>
  </div>
</template>

<script>
import Header from './components/Header'
import Main from './components/Main'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      links: ["Home", "Recipes", "Places", "Blog", "About", "Contact"],
    }
  }
}
</script>

<style lang="scss">
  @import '~bootstrap/scss/bootstrap.scss';
  @import '~@fortawesome/fontawesome-free/css/all.css';
  @import "./style/general.scss";

</style>
