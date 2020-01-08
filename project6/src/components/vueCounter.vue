<template>
  <div>
    
    <button @click="increment(100)">Increment</button>
    <button @click="decrement(50)">decrement</button>
    
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
    ...mapActions(['increment', 'decrement']),

    // increment: function () {
    //   return this.$store.commit('increment');
    // },
    // decrement: function () {
    //   return this.$store.commit('decrement');
    // }
    // increment: function (by) {
    //   this.$store.dispatch('increment', by)
    // }
  }
};
</script>

<style scoped>

</style>
