<template>
  <div>
    <h2>
      <div
        :class="{ winning: team1.score > team2.score, losing: team1.score < team2.score }"
      >{{ team1.name }}</div>vs
      <div
        :class="{ winning: team2.score > team1.score, losing: team2.score < team1.score }"
      >{{ team2.name }}</div>
    </h2>
  </div>
</template>

<script>
export default {
  props: ["team1", "team2"]
};
</script>

<style>
.winning {
  color: green;
}
.losing {
  color: red;
}
</style>