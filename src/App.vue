<template>
  <div id="app">
    <WebBackground />
    <ProductDisplay />
  </div>
</template>

<script>

import ProductDisplay from './components/ProductDisplay.vue';
import WebBackground from './components/WebBackground.vue';

export default {
  name: 'App',
  components: {
    ProductDisplay, WebBackground
  }
}
</script>

<style>
body {
  margin: 0;
}
</style>
