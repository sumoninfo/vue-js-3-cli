<template>
  <Card card_title="About Me">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda explicabo inventore ipsam porro rem?
      Assumenda atque autem blanditiis magnam maxime!</p>
  </Card>
  <Card card_title="Phone">
    <img src="https://v3.vuejs.org/logo.png" alt="">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur, hic.</p>
  </Card>
  <Card card_title="Services">
    <ul>
      <li>Web Development</li>
      <li>Software Development</li>
      <li>Mobile App</li>
    </ul>
  </Card>
</template>

<script>
import Card from "./components/Card";

export default {
  name      : 'App',
  components: {
    Card,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
