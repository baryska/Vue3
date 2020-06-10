<template>
  <div class="container">
    <div class="counter" v-on:click="addOne" v-bind:style="{ backgroundColor: color }">{{ number }}</div>
    <button v-on:click="reset">Reset</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  props: ["color", "max"],
  data() {
    return { number: 0 };
  },
  methods: {
    addOne() {
      if (this.number < this.max) {
        this.number += 1;
        this.$emit("oneUp");
      }
    },
    reset() {
      this.number = 0;
    }
  }
};
</script>

<style></style>
