<template>
  <input
    id="search"
    type="text"
    :value="value"
    @input="handleChange"/>
</template>

<script>
export default {
  name: 'SearchInput',
  props: {
    value: {
      type: String,
      required: true,
    },
  },
  methods: {
    handleChange(e) {
      this.$emit('input', e.target.value);
    },
  },
};
</script>

<style lang="scss" scoped>
  input {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 250px;
    height: 30px;
    margin: 50px 0 0 0;
    font-size: 18px;
    font-weight: 300;
    text-align: center;
    border: 0;
    border-bottom: 1px solid white;
    background: none;
    transition: box-shadow .3s ease-out;
    color: white;

    @media (min-width: 1024px) {
      font-weight: 400;
      width: 350px;
    }
  }

  input:focus {
    outline: none;
    box-shadow: 0 10px 20px -8px rgba(#fff, .5);
  }
</style>
