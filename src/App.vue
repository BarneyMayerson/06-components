<template>
  <div style="margin-bottom: 2rem;">
    <h3>Just do</h3>
    <Greetings :age="age" />
    <User :age="age" @age-changed="updateAge" :ageChangeFn="updateAgeCB"/>
  </div>
  <hr>
  <div style="margin-top: 2rem;">
    <AppForm>
      <template v-slot:help>
        <p>{{ help }}</p>
      </template>
      <template v-slot:fields>
        <input type="text" placeholder="email" />
        <input type="text" placeholder="username" />
        <input type="text" placeholder="password" />
      </template>
      <template v-slot:buttons>
        <button type="submit">Submit</button>
      </template>

      <p>Dummy</p>
    </AppForm>
    <hr>
    <AppForm>
      <template v-slot:help>
        <p>Contact help text.</p>
      </template>
      <template v-slot:fields>
        <input type="text" placeholder="name" />
        <input type="text" placeholder="message" />
      </template>
      <template v-slot:buttons>
        <button type="submit">Submit</button>
      </template>

      <p>Funny</p>
    </AppForm>
  </div>
</template>

<script>
import Greetings from "@/components/Greetings.vue";
import User from "@/components/User.vue";
import AppForm from "@/components/Form.vue";

export default {
  name: "App",

  components: {
    Greetings, User, AppForm,
  },

  data() {
    return {
      age: 20,
      help: "There help about this form.",
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
