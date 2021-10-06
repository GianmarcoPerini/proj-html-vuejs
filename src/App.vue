<template>
  <div id="app">
    
    <Heading />

    <mainWrapper />

    <Footing />

  </div>
</template>

<script>
import Heading from './components/Heading.vue';
import mainWrapper from './components/mainWrapper.vue';
import Footing from './components/Footing.vue';


export default {
  name: 'App',
  components: {
    Heading,
    mainWrapper,
    Footing,
    
  }
}
</script>



<style lang="scss">
@import '~bootstrap/scss/bootstrap';
@import '~@fortawesome/fontawesome-free/css/all.min.css';

</style>
