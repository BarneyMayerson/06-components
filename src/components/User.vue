<template>
  <p>The user is {{ age }} years old.</p>
  <button type="button" @click.prevent="age++">Update age</button>
</template>

<script>
export default {
  name: "User",

  props: ["age"],
}
</script>
