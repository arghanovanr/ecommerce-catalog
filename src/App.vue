<template>
  <div id="app">
    <div v-if="loading">
      <div class="view">
        <div class="loader"></div>
      </div>
    </div>

    <div v-else>
      <WebBackground :dataComponent=category />
      <ProductDisplay :dataComponent=data :dataCategory=category :getIndexProps="getIndex" />
      <button @click="getProductFromAPI()">KLIK</button>
      {{ index }}
    </div>

  </div>
</template>

<script>

import ProductDisplay from './components/ProductDisplay.vue';
import WebBackground from './components/WebBackground.vue';
export default {
  name: 'App',
  components: {
    ProductDisplay,
    WebBackground
  },
  data() {
    return {
      title: 'data',
      data: null,
      category:
      {
        man: null,
        woman: null,
        unavaliable: null,
      },
      loading: false,
      index: 1
    }
  },
  methods:
  {
    async getProductFromAPI() {
      if (this.index == 21) {
        this.index = 1;
      }
      this.loading = true;
      const api = await fetch(`https://fakestoreapi.com/products/${this.index}`);
      const response = await api.json();
      const data = response;
      alert("data bertambah 1")
      let product = { ...data }
      this.index++;
      if (product.category === "men's clothing") {
        this.category.man = true;
        this.category.woman = false;
        this.category.unavaliable = false;
      }
      else if (product.category === "women's clothing") {
        this.category.man = false;
        this.category.woman = true;
        this.category.unavaliable = false;
      }
      else {
        this.category.man = false;
        this.category.woman = false;
        this.category.unavaliable = true;
      }
      this.data = data;
      console.log(data);
      console.log(this.category)

      this.loading = false;

    }
  },
  mounted() {

    this.getProductFromAPI();

  }
}


</script>

<style>
/* Loader  */

.view {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.loader {
  border: 16px solid #f3f3f3;
  border-radius: 50%;
  border-top: 16px solid #3498db;
  width: 120px;
  height: 120px;
  animation: spin 2s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

/* css */
body {
  margin: 0;
}
</style>
