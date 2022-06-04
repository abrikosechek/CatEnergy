<template>
  <div id="app">
    <NavigationBar />
    <router-view />
  </div>
</template>

<script>
import NavigationBar from "./components/NavigationBar.vue";

export default {
  name: "App",
  components: { NavigationBar },
};
</script>

<style lang="scss">
$basic_green: #68b738;
$basic_green-2: #5eaa2f;
$basic_grey: #f2f2f2;
$special_grey-2: #ebebeb;
$special_grey-3: #cdcdcd;
$special_dark-grey: #444444;
$special_dark-grey-2: #222222;
$status_error: #ff8282;

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  font-family: Oswald, sans-serif;
}

body {
  margin: 0;
  min-height: 200vh;
}

* {
  box-sizing: border-box;

  * {
    &::-webkit-scrollbar {
      height: 0;
      width: 0;
    }
  }
}

h1,
h2,
h3,
h4,
h5,
h6,
p,
a,
span,
label {
  margin: 0;
  padding: 0;
}

h1 {
  font-size: 60px;
  font-weight: 400;
}

h2 {
  font-size: 20px;
  font-weight: 400;
}

a {
  text-decoration: none;
}

button {
  cursor: pointer;
  border-radius: 0;
}

.container {
  width: 100%;
  max-width: 1220px;
  margin: 0 auto;

  @media (max-width: 1220px) {
    padding: 0 20px;
  }

  @media (max-width: 480px) {
    padding: 0 10px;
  }
}
</style>
