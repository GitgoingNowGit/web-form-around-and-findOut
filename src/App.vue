<template>
<SignupForm />
</template>

<script>
import SignupForm from './Components/SignupForm.vue'

export default {
  name: 'App',
  components: {
    SignupForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body{
  margin: 0;
  background-color: #f0f0f0;
}
</style>
