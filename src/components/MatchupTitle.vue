<template>
  <div>
    <h2>{{team1.name}} vs {{team2.name}}</h2>
  </div>
</template>

<script>
export default {
  props: ["team1", "team2"]
};
</script>

<style>
</style>