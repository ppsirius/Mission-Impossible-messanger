<template>
  <div></div>
</template>

<script>
export default {
  components: {},
  async asyncData() {
    const date = new Date()
    let hash = `jedkl1321_${Math.floor((date.getTime() * 3) / 2)}`
    return  { hash }
  }
}
</script>

<style>
</style>
