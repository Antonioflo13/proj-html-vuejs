<template>
  <div id="app">
    <Header :links="links"/>
  </div>
</template>

<script>
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    Header,
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
