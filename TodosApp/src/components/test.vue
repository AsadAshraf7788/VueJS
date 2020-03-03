<template>
  <div>
    <p>{{ message }}</p>
    <p>{{email}}</p>
    <button v-on:click="reverseMessage">Reverse Message</button>
    <input type="email" v-model="email" class="bg-success">
    <button v-on:click="alert()" v-bind:disabled="email.length < 2">Submit</button>
   </div>
</template>

<script>
export default {
  name: 'test-comp',
  data () {
    return {
      message: 'Welcome to Vue!',
      email : ''
    }
  },
  methods: { 
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>