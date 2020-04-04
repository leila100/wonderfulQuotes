<template>
  <div class="container">
    <h1>Wonderful Quotes</h1>
    <NewQuote @quoteAdded="addQuote" />
    <QuoteGrid :quotes="quotes" />
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Info: Click on a quote to delete it!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";

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
    NewQuote,
  },
  methods: {
    addQuote(quote) {
      this.quotes.push(quote);
    },
  },
};
</script>

<style></style>
