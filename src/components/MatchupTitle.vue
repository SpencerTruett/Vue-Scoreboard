<template>
  <div>
    <h2>
      <span
        :class="{ winning: team1.score > team2.score, losing: team1.score < team2.score }"
      >{{ team1.name }}</span> vs
      <span
        :class="{ winning: team2.score > team1.score, losing: team2.score < team1.score }"
      >{{ team2.name }}</span>
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
h2 {
  font-size: 8vw;
  margin-bottom: 0;
}
</style>