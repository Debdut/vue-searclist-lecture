<template lang="pug">
  .search-list
    input(v-model="search")
    ul.list
      li.list-item(v-for="item in searchResults") {{ item }}
</template>

<script lang="ts">
export default {
  props: {
    data: Array,
    interval: Number,
  },
  data() {
    return {
      search: ''
    }
  },
  computed: {
    searchResults() {
      return this.data.filter(item => item.indexOf(this.search) === 0)
    }
  }
}
</script>

<style scoped>
  .list {
    list-style-type: none;
    -webkit-padding-start: 20px;
  }
</style>
