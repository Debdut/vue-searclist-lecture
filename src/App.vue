<template lang="pug">
  #app
    button(@click="updateWords()") Change Data
    search-list(:data="words")
</template>

<script>
import SearchList from "./components/SearchList";

export default {
  name: "App",
  components: {
    SearchList
  },
  data() {
    return {
      lapse: 2000,
      words: [
        "app",
        "apple",
        "apple juice",
        "appy",
        "mango",
        "man",
        "many",
        "any"
      ]
    };
  },
  methods: {
    updateWords() {
      this.words.shift();
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
