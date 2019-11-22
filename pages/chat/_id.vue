<template>
  <div></div>
</template>

<script>
export default {
  components: {},
  async asyncData(context) {
    const date = new Date()
    console.log(context)
    let hash = `box_${context.route.params.id}${Math.floor((date.getTime() * 3) / 2)}`
    return  { hash: hash }
  }
}
</script>

<style>
</style>
