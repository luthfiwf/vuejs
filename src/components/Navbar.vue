<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
    
        <a class="navbar-brand" href="#">Luwafaz</a>
       
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
           
          </ul>
           <!-- <ul class="navbar-nav ml-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link class="nav-link" to="/">Keranjang
              <b-icon-bag>     </b-icon-bag>
              <span class="badge badge-success ml-2">0</span>
              </router-link>
            </li>
          </ul> -->
        </div>
      </div>
   
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
</style>