<template>
  <Main />
  <button @click="roll">Roll Dice</button>
  <div>
    <span v-if="showDie">{{ die1 }} {{ die2 }}</span>
  </div>
</template>

<script>
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: { Main },

  data() {
    return {
      die1: null,
      die2: null,
      showDie: false,
    };
  },

  methods: {
    getRandom() {
      return Math.floor(Math.random() * 6 + 1);
    },

    roll() {
      this.die1 = this.getRandom();
      this.die2 = this.getRandom();
      this.showDie = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
