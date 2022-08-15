<template>
  <div>
    <center>
  <h1>{{count}}</h1>
 <button @click="increment">Increment</button>
 <button @click="reset">Reset</button>
    </center>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  computed:{
    count(){
      return this.$store.getters.getCount;
    }
  }, methods:{
    increment(){
      this.$store.dispatch('changeCount',1)
    },
    reset(){
      this.$store.dispatch('reset')
    }
  }
}
</script>

<style>

</style>
