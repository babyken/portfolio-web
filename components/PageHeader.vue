<template>
  <h1 class="title is-2 has-text-centered">
    {{ title }}
  </h1>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.title {
    font-family: 'Lacquer', Georgia, 'Roboto', Arial ;
    color: #555;
}
</style>
