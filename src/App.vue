<template>
  <div id="app">
    <div v-if="loading">
      <div class="view">
        <div class="loader"></div>
      </div>
    </div>

    <div v-else>
      <WebBackground :dataComponent=category />
      <ProductDisplay :dataComponent=data :dataCategory=category />
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
    }
  },
  methods:
  {
    async getProductFromAPI() {
      const api = await fetch('https://fakestoreapi.com/products/4');
      const response = await api.json();
      const data = response;



      let product = { ...data }
      if (product.category === "men's clothing") {
        this.category.man = true;
      }
      else if (product.category === "women's clothing") {
        this.category.woman = true;
      }
      else {
        this.category.unavaliable = true;
      }

      console.log(data);
      console.log(this.category)
      return data;
    }
  },
  mounted() {
    ((async () => {
      this.loading = true;
      this.data = await this.getProductFromAPI();
    })()).catch(console.error).finally(() => (this.loading = false));
  }
}


</script>

<style>
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

body {
  margin: 0;
}
</style>
