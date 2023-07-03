<template>
  <div style="margin-bottom: 2rem;">
    <h3>Just do</h3>
    <Greetings :age="age" />
    <User :age="age" @age-changed="updateAge" :ageChangeFn="updateAgeCB"/>
  </div>
  <hr>
  <div style="margin-top: 2rem;">
    <AppForm>
      <div class="help">
        <p>There is help about this form.</p>
      </div>
      <div class="fields">
        <input type="text" placeholder="email" />
        <input type="text" placeholder="username" />
        <input type="text" placeholder="password" />
      </div>
      <div class="buttons" style="margin-top: 12px;">
        <button type="submit">Submit</button>
      </div>
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
