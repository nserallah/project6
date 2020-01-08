<template>
  <div id="app">
    <h1>Vuex</h1>
    <result-counter></result-counter>
    <another-result></another-result>
    <vue-counter></vue-counter>
    <another-counter></another-counter>
    <br />
    <input type="text" v-model="value">
    <p>{{ value }}</p>
    
  </div>
</template>

<script>
export default {
  data: function() {
    return {
     
    };
  },
  computed: {
    value: {
      get() {
        return this.$store.getters.value;
      },
      set(value) {
        this.$store.dispatch('updateValue', value)
      }
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
