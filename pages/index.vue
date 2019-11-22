<template>
  <div class="container">
    <home />
  </div>
</template>

<script>
import Home from '~/components/home.vue'

export default {
  components: {
    Home
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
