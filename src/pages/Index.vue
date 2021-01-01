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
    title: 'NAB Big12'
  },

  components: {
    Hero,
    Features
  }

}
</script>

