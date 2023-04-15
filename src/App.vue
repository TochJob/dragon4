<template>
  <div id="app">
    <Header/>
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
export default {
  name: 'App',
  components: {
    Header, 
  }
}

</script>

<style>
@import '@/assets/css/fonts.scss';
* {
  margin: 0%;
  padding: 0%;
  box-sizing: border-box;
}
</style>
