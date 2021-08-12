<template>
  <div class="card" >
    <!-- <img :src="'assets/images/' + product.gambar " class="card-img-top" alt="..." /> -->
    <!-- {{product.url}} -->
    <img v-bind:src="product.download_url" alt="">
    <div class="card-body">
      <h5 class="card-title">{{product.author}}</h5>
     
    </div>
  </div>
  <!-- <h2>Card Produk {{ product.nama }}</h2> -->
</template>

<script>
export default {
  name: "CardProduct",
  props: ["product"],
};
</script>

<style>
</style>