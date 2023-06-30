<template>
  <p v-if="age >= 25">{{ msg }}</p>
  <p v-else>You must be 25 years or older to view this message.</p>
</template>

<script>
export default {
  name: "Greetings",

  props: ["age"],

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
