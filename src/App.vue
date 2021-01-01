<template>
  <body>
    <div id="app">
      <app-home></app-home>
    </div>
  </body>
</template>

<script>
import Home from "./components/Home"
export default {
  name: "App",
  components: {
   appHome:Home
  },
};
</script>

<style scoped>
  *{
    box-sizing: border-box;
  }
  body{
    margin: 0;
    padding: 0;
  }
</style>>

