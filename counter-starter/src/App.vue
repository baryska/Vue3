<template>
  <div class="container">
    <h1>Já jsem Vue aplikace</h1>
    <MyCounter color="yellow" max="5" v-on:oneUp="addToSum" v-on:reset="changeSum" />
    <MyCounter color="red" max="8" v-on:oneUp="addToSum" v-on:reset="changeSum" />
    <MyCounter color="blue" max="7" v-on:oneUp="addToSum" v-on:reset="changeSum" />
    <MyCounter color="#000" max="3" v-on:oneUp="addToSum" v-on:reset="changeSum" />
    <p>Celkový součet je {{ counterSum }}</p>
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
export default {
  name: "App",
  components: {
    MyCounter: Counter
  },
  data() {
    return { counterSum: 0 };
  },
  methods: {
    addToSum() {
      this.counterSum++;
    },
    changeSum(difference) {
      this.counterSum -= difference;
    }
  }
};
</script>

<style lang="css">
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

.counter {
  width: 3rem;
  height: 3rem;
  margin: 1rem 2rem;
  line-height: 3rem;
  text-align: center;
  font-size: 1.8rem;
  border-radius: 0.5rem;
  color: white;
  background-color: orange;
}
</style>
