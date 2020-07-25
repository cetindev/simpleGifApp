<template>
  <div class="search">
    <input
      type="text"
      v-model="query"
      @keypress.enter="handleSearch"
      placeholder="Please Write Here..."
    />
    <button @click="handleSearch">Search</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      query: "",
    };
  },
  methods: {
    handleSearch() {
      this.$emit("SearchRequested", this.query);
    },
  },
};
</script>

<style>
body {
  background-color: rgb(240, 236, 236);
}
.search {
  text-align: center;
  margin: 50px 5px;
}
.search input {
  padding: 10px 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  width: 400px;
}
.search button {
  padding: 5px 15px;
  border: 1px solid #ccc;
  background-color: #4183c4;
  color: #fff;
  font-size: 16px;
  border-radius: 5px;
}
</style>
