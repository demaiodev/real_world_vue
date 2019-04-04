<template>
  <h1>Showing Event #{{ id }}</h1>
</template>

<script>
export default {
  props: {
    id: {
      type: Number,
      default: null
    }
  },
  data() {
    return {
      key: 'value'
    }
  }
}
</script>

<style></style>
