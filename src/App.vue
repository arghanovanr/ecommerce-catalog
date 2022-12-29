<template>
  <div id="app">
    <WebBackground :dataComponent=data />
    <ProductDisplay :dataComponent=data />
  </div>
</template>

<script>

import ProductDisplay from './components/ProductDisplay.vue';
import WebBackground from './components/WebBackground.vue';

export default {
  name: 'App',
  components: {
    ProductDisplay, WebBackground
  },
  data() {
    return {
      title: 'data',
      data:
      {
        man: true,
        woman: false,
        rating: 5,
        productName: "Lock and Love Women's Removable Hooded Faux Leather Moto Biker Jacket",
        category: "women's clothing",
        description: "100% POLYURETHANE(shell) 100% POLYESTER(lining) 75% POLYESTER 25% COTTON (SWEATER), Faux leather material for style and comfort / 2pockets of front, 2-For-One Hooded denim style faux leather jacket,Button detail on waist / Detail stitching at sides, HAND WASH ONLY / DO NOT BLEACH / LINE DRY / DO NOT IRON",
        price: "$29,95",
        image: "https://fakestoreapi.com/img/81XH0e8fefL._AC_UY879_.jpg"
      }
    }
  }
}
</script>

<style>
body {
  margin: 0;
}
</style>
