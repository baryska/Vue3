<template>
  <aside class="menu">
    <div class="menu__item" @click="changeName">Domů</div>
    <div class="menu__item" @click="changeName">Blog</div>
    <div class="menu__item" @click="changeName">Kontakt</div>
  </aside>
</template>

<script>
export default {
  name: "Menu",

  methods: {
    changeName(event) {
      this.$emit("rename", event.target.textContent);
    }
  }
};
</script>

<style lang="css">
.menu {
  padding-top: 2rem;
  flex: 0 0 12rem;
  width: 12rem;
  height: 100%;
  background-color: deepskyblue;
  color: #555;
}

.menu__item {
  line-height: 2rem;
  padding: 0 2rem;
}
</style>