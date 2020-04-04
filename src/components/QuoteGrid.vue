<template>
  <div class="row">
    <div v-for="quote in quotes" :key="quote">
      <Quote>{{ quote }}</Quote>
    </div>
  </div>
</template>

<script>
import Quote from "./Quote.vue";
export default {
  props: ["quotes"],
  components: {
    Quote,
  },
};
</script>

<style></style>
