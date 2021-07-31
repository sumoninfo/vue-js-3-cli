<template>
  <Article/>
  <hr>
  <Card card_title="About Me">
    <template v-slot:default>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda explicabo inventore ipsam porro rem?
        Assumenda atque autem blanditiis magnam maxime!</p>
    </template>
    <template v-slot:footer>
      <a>Read more</a>
    </template>
  </Card>
  <Card card_title="Phone">
    <template v-slot:default>
      <img src="https://v3.vuejs.org/logo.png" alt="">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur, hic.</p>
    </template>
  </Card>

</template>

<script>
import Card    from "./components/Card";
import Article from "@/components/Article";

export default {
  name      : 'App',
  components: {
    Article,
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
