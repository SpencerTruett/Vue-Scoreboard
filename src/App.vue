<template>
  <div id="app">
    <MatchupTitle :team1="team1" :team2="team2" />
    <GameStatus :team1="team1" :team2="team2" />
    <div class="scores">
      <ScoreCard
        :score="team1.score"
        @pointsIncrease="updateScore(team1, 1)"
        @pointsDecrease="updateScore(team1, -1)"
      />

      <ScoreCard
        :score="team2.score"
        @pointsIncrease="updateScore(team2, 1)"
        @pointsDecrease="updateScore(team2, -1)"
      />
    </div>
  </div>
</template>

<script>
import MatchupTitle from "./components/MatchupTitle";
import ScoreCard from "./components/ScoreCard";
import GameStatus from "./components/GameStatus";

export default {
  components: {
    MatchupTitle,
    ScoreCard,
    GameStatus
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

<style>
body {
  background-color: #2c3e50;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgba(255, 255, 255, 0.8);
  margin-top: 60px;
}
.scores {
  display: flex;
  justify-content: space-evenly;
}
</style>
