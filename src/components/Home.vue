<template>
   <div>
       <h1>Server Status : {{ status }}</h1>
       <button @click="changeStatus">Change Status</button>
   </div>
</template>

<script>
export default {
    data: function() {
        return {
            status: 'Critical'
        }
    },
    methods: {
        changeStatus: function() {
            this.status = 'Running'
        }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
