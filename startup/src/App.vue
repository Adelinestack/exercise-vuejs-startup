<template>
  <div id="app">
    <img
      alt="Vue logo"
      src="https://images.unsplash.com/photo-1559116857-9ef933b15fff?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
    >
    <h1>Première app en Vue.js</h1>
    <HelloWorld url="https://unsplash.com/" texte="Site unsplash" bool="true"/>
    <BgModifier/>
    <BgButtonModifier/>
    <BgButtonsModifier/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import BgModifier from "./components/BgModifier";
import BgButtonModifier from "./components/BgButtonModifier";
import BgButtonsModifier from "./components/BgButtonsModifier";

export default {
  name: "app",
  components: {
    HelloWorld,
    BgModifier,
    BgButtonModifier,
    BgButtonsModifier
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
