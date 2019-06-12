<template>
  <div>
    <home></home>    
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
