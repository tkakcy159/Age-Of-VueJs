<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id:</label>
      <input type="text" id="username" v-model="username">
    </div>
    <div>
      <label for="password">pw:</label>
      <input type="password" id="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios'

export default {
  data: fu nction () {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function() {
      // event.preventDefault();

      console.log(this.username);
      console.log(this.password);
      
      var url = "https://jsonplaceholder.typicode.com/users";
      var data = {
        username: this.username,
        password: this.password
      }

      axios.post(url, data)
        .then(function(res) {
          console.log(res);
        })
        .catch(function(err) {
          console.log(err);
        });
    }
  }
}
</script>

<style>

</style>