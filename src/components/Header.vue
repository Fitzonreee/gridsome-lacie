<template>
  
    <header class="header container">
      <nav class="nav">
        <Logo/>
      </nav>
    </header>

</template>

<script>
import Logo from './Logo'

export default {
    name: 'Header',
    components: {
        Logo
    }
}
</script>



<style lang="scss">

.header {
  height: 60px;
  display: flex;
  align-items: center;
  padding-top: 0.5em;

  @include medium {
    height: 80px;
    padding-top: 1.25em;
  }

}

.nav {
  display: flex;
  align-items: center;

  svg {
      margin-left: 15px;
      width: 80px;
  }
}

</style>
