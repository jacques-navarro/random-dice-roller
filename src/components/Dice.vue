<template>
  <div class="container" v-layout>
    <div class="dice left">{{ die1 }}</div>
    <div class="dice">{{ die2 }}</div>
  </div>
</template>

<script>
export default {
  props: ["die1", "die2"],
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  width: 150px;
  line-height: 50px;
}

.dice {
    min-width: 0;
    margin: auto;
  width: 50px;
  border-radius: 10px;
  background: #0faf87;
  color: white;
  font-size: 22px;
}
</style>
