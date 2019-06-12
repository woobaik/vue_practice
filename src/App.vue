<template>
  <h1>Server Status: {{ status }} </h1>
  
</template>

<script>
export default {
  name: 'app',
  data: function() {
    return {
      status: 'Critical'
    }
  }
}
</script>

<style>

</style>
