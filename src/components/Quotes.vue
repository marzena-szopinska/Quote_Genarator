<template>
  <div>
    <h1>Quotes Component</h1>
    <quote-app v-for="(quote, index) in quoteList" v-bind:key="index">
      <h2>{{index + 1}}. {{quote}}</h2>
    </quote-app>
  </div>
</template>

<script>
import Quote from "./Quote";

export default {
  props: ["quoteList"],
  components: {
    quoteApp: Quote
  }
};
</script>

<style scoped>
</style>