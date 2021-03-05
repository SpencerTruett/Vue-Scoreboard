<template>
  <div>{{gameLeaderDisplay}}</div>
</template>

<script>
export default {
  props: ["team1", "team2"],

  computed: {
    gameLeaderDisplay() {
      const { team1, team2 } = this.$props;

      if (team1.score > team2.score) {
        const scoreDiff = team1.score - team2.score;
        if (scoreDiff > 1) {
          return `${team1.name} is leading ${team2.name} by ${scoreDiff} points!`;
        } else {
          return `${team1.name} is leading ${team2.name} by ${scoreDiff} point!`;
        }
      }
      if (team1.score < team2.score) {
        const scoreDiff = team2.score - team1.score;
        if (scoreDiff > 1) {
          return `${team2.name} is leading ${team1.name} by ${scoreDiff} points!`;
        } else {
          return `${team2.name} is leading ${team1.name} by ${scoreDiff} point!`;
        }
      }

      return "The game is tied!";
    }
  }
};
</script>

<style>
</style>