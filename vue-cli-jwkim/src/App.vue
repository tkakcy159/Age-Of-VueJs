<template>
  <div>
    <app-header 
      v-bind:msg="str"
      v-on:renew="renewString"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'

export default {
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewString: function() {
      this.str='hi';
    }
  }
}
</script>

<style>

</style>