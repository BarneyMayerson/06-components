<template>
  <div>
    <h3>Just do</h3>
    <Greetings :age="age" />
    <User :age="age" />
  </div>
</template>

<script>
import Greetings from "@/components/Greetings.vue";
import User from "@/components/User.vue";

export default {
  name: "App",

  components: {
    Greetings, User
  },

  data() {
    return {
      age: 20,
    }
  }
}
</script>
