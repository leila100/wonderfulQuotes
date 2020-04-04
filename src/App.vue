<template>
  <div>
    <h1>Wonderful Quotes</h1>
    <QuoteGrid :quotes="quotes" />
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
export default {
  name: "App",
  data() {
    return {
      quotes: ["Just a quote to see something"],
      maxQuotes: 10,
    };
  },
  components: {
    QuoteGrid,
  },
};
</script>

<style></style>
