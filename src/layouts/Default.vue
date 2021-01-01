<template>
  <div class="layout">
    <Header/>
    <slot/>
    <Footer/>
  </div>
</template>

<script>
import Footer from '../components/Footer'
import Header from '../components/Header'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">

@font-face {
  font-family: Futura-book-bt;
  src: url('../assets/fonts/futura-book-bt.ttf');
}

body {
  font-family: 'Futura-book-bt', sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  /* This could be the container */
}


</style>
