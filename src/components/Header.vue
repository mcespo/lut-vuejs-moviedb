<template>
  <header>
    <h1>{{currentTime}}</h1>
  </header>
</template>

<script>
  export default {
    name: 'Header',
    data(){
      return {
         currentTime: new Date().toLocaleString([], {
            month: 'short',
            day: '2-digit',
            year: 'numeric',
            hour: '2-digit',
            minute: '2-digit'
         })
      }
   },
   created: function() {
      setInterval(() => {
         this.updateCurrentTime();
      }, 1000);
   },
   methods: {
      updateCurrentTime: function() {
         this.currentTime = new Date().toLocaleString([], {
            month: 'short',
            day: '2-digit',
            year: 'numeric',
            hour: '2-digit',
            minute: '2-digit'
         });
      }
   },
  }
</script>

<style scoped>
  header {
    background: #111;
    padding: 20px;
    color: #fff;
  }
  h1 {
    margin: 0;
  }
</style>