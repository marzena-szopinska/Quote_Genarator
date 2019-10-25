<template>
  <!-- Here the App will render three components dynamicaly -->
  <div>
    <header>
      <nav>
        <button>Home</button>
        <button>About</button>
        <button>Add Quote</button>
      </nav>
    </header>
    <hr />
  </div>
</template>

<script>
import Quotes from "./components/Quotes";
import About from "./components/About";
import NewQuote from "./components/NewQuote";

export default {
  data() {
    return {
      selectedComponent: "quoteApp",
      quotes: ["Quote number one", "Quote number two", "Quote number three"]
    };
  },
  components: {}
};
</script>

<style scoped>
</style>