<template>
  <Layout>

    <Hero/>
    <Features/>

  </Layout>
</template>

<script>
import Hero from '../components/Hero'
import Features from '../components/Features'

export default {
  
  metaInfo: {
    title: 'Hello, world!'
  },

  components: {
    Hero,
    Features
  }

}
</script>

<style lang="scss">

@import url('https://fonts.googleapis.com/css?family=Raleway:300,400,700,800&display=swap');

.layout {
  font-family: 'Raleway', sans-serif;
}

</style>
