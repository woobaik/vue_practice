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
      <transition name="slide" type="animation">
       <p v-if="show" class="sample">
         This is a sample test
      </p>
    </transition>
      <transition name="slide" appear>
       <p v-if="show" class="sample">
         
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

  .slide-enter {
    transform: translateY(20px);
  }

  .slide-enter-active {
    animation: slide-in 1s ease-in-out forwards;
  }

  .slide-leave {
    transform: translateY(0)
  }

  .slide-leave-active {
    animation: slide-out 1s ease-in-out forwards;
  }

  @keyframes slide-in {
    from { transform: translateY(20px)}
    to { transform: translateY(0)}
  }

  @keyframes slide-out {
    from { transform: translateY(0)}
    to { transform: translateY(20px)}
  }
</style>
