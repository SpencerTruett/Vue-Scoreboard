<template>
  <div id="app">
    <MatchupTitle :team1="team1" :team2="team2" />
    <ScoreCard :score="team1.score" />
    <ScoreCard :score="team2.score" />
  </div>
</template>

<script>
import MatchupTitle from "./components/MatchupTitle";
import ScoreCard from "./components/ScoreCard";

export default {
  components: {
    MatchupTitle,
    ScoreCard
  },
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

<style></style>
