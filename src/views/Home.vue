<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />
      <div class="row mt-4">
        <div class="col">
          <h2>
            Best
            <strong>Produk</strong>
          </h2>
        </div>
      
      </div>
      <div class="row mb-3">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
          <CardProduct :product="product"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    CardProduct,
  },

  data() {
    return {
      products: [],
      page: 1
    };
  },

  methods: {
    setProduct(data) {
      this.products = data;
    },
  },

  mounted() {
    axios
      .get("https://picsum.photos/v2/list?page=${this.page}&limit=100")
      .then((response) => this.setProduct(response.data))
      .catch((error)  => console.log(error))
     
  },
  handleScrolledToBottom (isVisible) {
    if (!isVisible) {return}

    this.page++
    this.fetch()
  }
};
</script>
