<template>
  <div>
    <home v-for="server in 5">{{server}}</home>    
  </div>
  
</template>

<script>
import Home from './components/Home'
export default {
  name: 'app',
  data: function() {
    return {
      status: 'Critical'
    }
  },
  components: {
    'home': Home
  }
}
</script>

<style>

</style>
