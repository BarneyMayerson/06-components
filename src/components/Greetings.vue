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

<style scoped lang="scss">
  p:hover {
    color: lighten(black, 33%);
  }
</style>
