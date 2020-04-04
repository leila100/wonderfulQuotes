<template>
  <div class="container">
    <h1>Wonderful Quotes</h1>
    <Header :quoteCount="quotes.length" :maxQuotes="maxQuotes" />
    <NewQuote @quoteAdded="addQuote" />
    <QuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote" />
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
import Header from "./components/Header.vue";

export default {
  name: "App",
  data() {
    return {
      quotes: [
        " Nothing will bring you peace, you must bring yourself to it.",
        "Never let success get to your head, and never let failure get to your heart.",
      ],
      maxQuotes: 4,
    };
  },
  components: {
    QuoteGrid,
    NewQuote,
    Header,
  },
  methods: {
    addQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("You have reached the maximum. Please delete some quotes to add more.");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    },
  },
};
</script>

<style></style>
