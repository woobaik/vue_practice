<template>
  <div>
    <h1>Practice Name :: {{ title }}</h1>  

    <hr>
    <button @click="show=!show">{{ button }}</button>
     value check [ {{ show }} ]

     <p v-if="show" class="sample">
       This is a sample test
     </p>
  </div>
  
</template>

<script>
export default {
  data: function() {
    return {
      title: 'Animation',
      button: 'Show / Hide',
      show: true
    }
  }
}
</script>

<style>
  .sample {
    background-color: lightcoral;
    border: 4px solid black;
  }
</style>
