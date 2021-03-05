<template>
  <div>
    <h1>{{ score }}</h1>
    <div>
      <button>-</button>
      <button>+</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["score"]
};
</script>

<style>
</style>