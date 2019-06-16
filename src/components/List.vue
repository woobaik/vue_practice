<template>
  <div>

      <label for="fruit">Fruit :</label>
      <input type="text" name="fruit" id="fruit" v-model="input">
      
      <ul>
        <li v-for="fruit in filteredFruits" v-bind:key="fruit">{{fruit}}</li>
      </ul>
  </div>
  
</template>

<script>

  export default {
    data: function() {
      return {
        fruits: ['Apple', 'Banana', 'Pear', 'Melon'],
        input: ''
      }
    },
    filters: {
      toUpperCase: (text) => {
        return text.toUpperCase()
      }
    },
    computed: {
      filteredFruits() {
        return this.fruits.filter( (fruit) => {
          return fruit.match(this.input)  
        })
      }
    }
  }
</script>

<style>

</style>
