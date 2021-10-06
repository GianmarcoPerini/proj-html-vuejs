<template>
  <div id="app">
    
    <Heading />

    <mainWrapper />

    <Footing />

  </div>
</template>

<script>
import Heading from './components/Header/heading';
import mainWrapper from './components/Main/mainWrapper.vue';
import Footing from './components/Footer/footing';


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
@import './components/fonts/font.scss';


#app{
  font-family: 'Varela Round', sans-serif;
  }

</style>
