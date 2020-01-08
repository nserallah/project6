<template>
  <div>
    
    <button @click="asyncIncremrent({by: 50, duration: 1000})">Increment</button>
    <button @click="asyncDecrement({by: 50, duration: 1000})">decrement</button>
    
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "emitTest",
  data: function() {
    return {
      
    }
  },
  methods: {
      ...mapActions(['asyncIncremrent', 'asyncDecrement'])
    // increment: function () {
    //   return this.$store.commit('increment');
    // },
    // decrement: function () {
    //   return this.$store.commit('decrement');
    // }
  }
};
</script>

<style scoped>

</style>
