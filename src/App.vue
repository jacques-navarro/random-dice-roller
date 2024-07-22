<template>
  <Main />
  <button @click="roll">Roll Dice</button>
  <Dice class="center" v-if="showDie" :die1="die1" :die2="die2" />
</template>

<script>
import Main from "./components/Main.vue";
import Dice from "./components/Dice.vue";

export default {
  name: "App",
  components: { Main, Dice },

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

      console.log(`${this.die1} ${this.die2}`);

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
