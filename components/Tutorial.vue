<!-- Please remove this file from your project -->
<template>
  <div>
  <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand href="javascript:void(0)">NavBar</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="/products">Products (SSR)</b-nav-item>
        <nuxt-link to="/products/1111" tag="b-nav-item">Products</nuxt-link>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form @submit.prevent>
          <b-form-input v-model="productId" size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit" @click="showProduct">Search Product</b-button>
        </b-nav-form>

      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: 'NuxtTutorial',
  data(){
    return{
      productId : null,
    }
  },
  methods:{
    showProduct(){
      this.$router.push("/products/" + this.productId)
    }
  }
}
</script>
