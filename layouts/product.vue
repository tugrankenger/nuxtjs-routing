<template>
  <div>
    <Nuxt /> 
    <footer :text="['center', 'lg-start']">
      <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2)">
        © 2023 Copyright:
        <a class="text-dark" target="_blank" href="https://github.com/tugrankenger"> tugrankenger</a>
      </div>
    </footer>
  </div>
</template>

<style scoped>
  footer{
    position: fixed;
    bottom: 0;
    width: 100%;
  }
</style>