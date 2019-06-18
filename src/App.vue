<template>
  <div>
    <h1>{{ happy }} </h1>
    <button @click="happy = !happy">Show/Hide</button>
    <br>
    <transition name="fade">
      <p class="para" v-if="happy">
        Happiness is what I want
      </p>
    </transition>
    
  </div>  
</template>

<script>
export default {
  data: function() {
    return {
      happy: true
    }
  }
}
</script>

<style>
  .para {
    background-color: red; 
  }
  .fade-enter {
    opacity: 0;
  }

  .fade-enter-active {
    transition: opacity 1s;
  }

  .fade-leave {
    
  }

  .fade-leave-active {
    transition: opacity 1s;
    opacity: 0
  }
</style>
