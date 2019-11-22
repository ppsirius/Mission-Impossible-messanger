<template>
  <div class="container"></div>
</template>

<script>
export default {
  components: {},
  async asyncData({ $axios }) {
    const jsonBox = await $axios.$get('/box_f1b0dfa4b996525949e9')
    return { jsonBox }
  },
  data() {
    return {}
  },
  mounted() {
    console.log(this.jsonBox)
  }
}
</script>

<style>
</style>
