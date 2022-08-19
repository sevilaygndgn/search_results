<template>
  <div class="container">
    <div class="search">
      <input class="search-input" v-model="search" @change="emitSearchValue" />
      <button class="search-button">
        <svg
          width="25"
          height="25"
          viewBox="0 0 29 29"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M12.0833 20.5417C16.7547 20.5417 20.5417 16.7547 20.5417 12.0833C20.5417 7.41192 16.7547 3.625 12.0833 3.625C7.41192 3.625 3.625 7.41192 3.625 12.0833C3.625 16.7547 7.41192 20.5417 12.0833 20.5417Z"
            stroke="white"
            stroke-width="1.8125"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M25.375 25.375L18.125 18.125"
            stroke="white"
            stroke-width="1.8125"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </button>
    </div>
    <product-list />
  </div>
</template>

<script>
import { eventBus } from "@/main";
import ProductList from "@/components/ProductList.vue";
export default {
  components: { ProductList },
  data() {
    return {
      search: "",
    };
  },
  methods: {
    emitSearchValue() {
      eventBus.$emit("searchProduct", this.search);
    },
  },
};
</script>
<style lang="scss" scoped>
.container {
  background-color: #f1f4ff;
  padding-top: 100px;
  height: 270px;
  width: 500px;
  display: grid;
  row-gap: 10px;
  justify-content: center;
  border-radius: 10px;
  .search {
    display: flex;
  }
  .search-input {
    width: 300px;
    height: 45px;
    background-color: #ffffff;
    border: none;
    border-top-left-radius: 16px;
    border-bottom-left-radius: 16px;
    padding-left: 20px;
    &:focus {
      outline: none;
    }
  }
  .search-button {
    width: 45px;
    height: 45px;
    border: none;
    border-top-right-radius: 16px;
    border-bottom-right-radius: 16px;
    background-color: #2c3e50;
    display: flex;
    justify-content: center;
    align-items: center;
    &:hover {
      cursor: pointer;
    }
  }
}
</style>
