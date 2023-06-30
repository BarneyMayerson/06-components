<template>
  <p>{{ msg }}</p>
</template>

<script>
export default {
  name: "Greetings",

  data() {
    return {
      msg: "Hello there.",
    }
  }
}
</script>

<style scoped>
  p {
    color: red;
  }
</style>
