<template>
  <p>The user is {{ age }} years old.</p>
  <p>{{ ageDouble }} : doubled!</p>
  <button type="button" @click.prevent="onClickAge">Update age Event</button>
  <button type="button" @click.prevent="ageChangeFn(5)">Update age Callback</button>
</template>

<script>
export default {
  name: "User",

  props: {
    age: {
      type: Number,
      // required: true,
      validaror(value) {
        return value < 130;
      },
    },
    ageChangeFn: Function,
  },

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
