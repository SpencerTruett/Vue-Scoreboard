<template>
  <div id="app">
    <MatchupTitle :team1="team1" :team2="team2" />
    <ScoreCard
      :score="team1.score"
      @addPoint="updateScore(team1, 1)"
      @subtractPoint="updateScore(team1, -1)"
    />

    <ScoreCard
      :score="team2.score"
      @addPoint="updateScore(team2, 1)"
      @subtractPoint="updateScore(team2, -1)"
    />
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
  },
  methods: {
    updateScore(team, points) {
      const theUpdatedScore = team.score + points;

      if (theUpdatedScore >= 0) {
        team.score = theUpdatedScore;
      }
    }
  }
};
</script>

<style></style>
