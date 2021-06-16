<template>
  <div class="searchWrapper">
    <div class="search">
      <input
        id="search"
        type="text"
        v-model="searchValue"
        @input="handleInput" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchInput',
};
</script>

<style lang="scss" scoped>
  .searchWrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 50px 0 0 0;
    padding: 30px;
    width: 100%;
  }

  .search {
    display: flex;
    flex-direction: column;
    width: 300px;

    input {
      height: 30px;
      border: 0;
      border-bottom: 1px solid black;
      background: none;
    }
  }
</style>
