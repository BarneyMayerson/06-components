<template>
  <div>
    <h3>Just do</h3>
    <Greetings :age="age" />
    <User :age="age" @age-changed="updateAge" :ageChangeFn="updateAgeCB"/>
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
  },

  methods: {
    updateAge(num) {
      if (!num) return
      
      this.age += num;
    },
    updateAgeCB(num) {
      if (!num) return
      
      this.age += num;
    }    
  },
}
</script>
