<template>
  <div>
    <dvi>
      <h2>{{team1.name}}</h2>
      <div>
        <button>-</button>
        <button>+</button>
      </div>
    </dvi>
    <div>
      <h2>{{team2.name}}</h2>
      <button>-</button>
      <button>+</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team1: {
        name: "Team 1",
        score: 0
      },
      team2: {
        name: "Team 2",
        score: 0
      }
    };
  }
};
</script>

<style>
</style>