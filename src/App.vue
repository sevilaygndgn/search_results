<template>
  <div id="app">
      <router-view />
  </div>
</template>
<script>
import HomeView from "./views/HomeView";
export default {
 // components: { HomeView },
};
</script>
<style lang="scss">
@import "./assets/reset.scss";
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
body {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Poppins', sans-serif;
}
</style>
