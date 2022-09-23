<template>
<gym-form />
<!-- <fetch-data /> -->
</template>

<script>
// import FetchData from './components/FetchData.vue'
import GymForm from './components/GymForm.vue'

export default {
  name: 'App',
  components: {
    GymForm,
    // FetchData
    
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
</style>
