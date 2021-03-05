<template>
  <div>
    <h1>{{ score }}</h1>
    <div>
      <button @click="subtractPoint">-</button>
      <button @click="addPoint">+</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["score"],

  methods: {
    addPoint() {
      this.$emit("pointsIncrease");
    },
    subtractPoint() {
      this.$emit("pointsDecrease");
    }
  }
};
</script>

<style>
</style>