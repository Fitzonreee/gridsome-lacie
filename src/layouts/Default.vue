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

<style>
body {
  font-family: 'Futura-medium', sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  /* This could be the container */
}


</style>
