<template>
  <!-- Here the App will render three components dynamicaly -->
  <div>
    <header>
      <nav>
        <button @click="selectedComponent = 'quotesApp'">Home</button>
        <button @click="selectedComponent = 'aboutApp'">About</button>
        <button @click="selectedComponent = 'newQuoteApp'">Add Quote</button>
      </nav>
    </header>
    <hr />
    <component v-bind:is="selectedComponent"></component>
  </div>
</template>

<script>
import Quotes from "./components/Quotes";
import About from "./components/About";
import NewQuote from "./components/NewQuote";

export default {
  data() {
    return {
      selectedComponent: "quotesApp",
      quotes: ["Quote number one", "Quote number two", "Quote number three"]
    };
  },
  components: {
    quotesApp: Quotes,
    aboutApp: About,
    newQuoteApp: NewQuote
  }
};
</script>

<style scoped>
</style>