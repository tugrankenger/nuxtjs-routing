<template>
  <div>
      <p>id info: {{ $route.params.productId }}</p>
  </div>
</template>

<script>
  export default{
    validate(arg){
      console.log(arg)
      // return arg.params.productId == "tugran"
      return /^\d+$/.test(arg.params.productId)
    }
  }
</script>