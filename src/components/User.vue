<template>
  <p>The user is {{ age }} years old.</p>
  <p>{{ ageDouble }} : doubled!</p>
  <button type="button" @click.prevent="onClickAge">Update age</button>
</template>

<script>
export default {
  name: "User",

  props: ["age"],

  emits: ["age-changed"],

  computed: {
    ageDouble() {
      return this.age * 2;
    }
  },

  methods: {
    onClickAge() {
      this.$emit("age-changed", 2);
    }
  },
}
</script>
