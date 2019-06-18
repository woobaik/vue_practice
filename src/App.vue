<template>
  <div>
    <h1>Practice Name :: {{ title }}</h1>  

    <hr>
    <button @click="show=!show">{{ button }}</button>
     value check [ {{ show }} ]
    <transition name="fade">
      <p v-if="show" class="sample">
       This is a sample test
     </p>
    </transition>
     
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

  .fade-enter {
    opacity: 0;
  }

  .fade-enter-active {
    transition: opacity 1s;
  }

  .fade-leave {
    opacity: 1;
  }

  .fade-leave-active {
    transition: opacity 1s;
    opacity: 0;
  }
</style>
