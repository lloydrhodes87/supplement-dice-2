<template>
  <div>
    <h1>Random numbers and Letters</h1>
    <div id="app">
      <HelloWorld/>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: "Cinzel", serif;
}
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  background-color: #c60b1e;
  color: white;
  padding: 50px;
  margin: 0;
  text-align: center;
}
body {
  background-color: #ffc400;
}
</style>
