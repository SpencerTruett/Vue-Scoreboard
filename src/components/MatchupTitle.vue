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
import { team1 } from "../data";
import { team2 } from "../data";

export default {
  data() {
    return {
      team1: team1,
      team2: team2
    };
  }
};
</script>

<style>
</style>