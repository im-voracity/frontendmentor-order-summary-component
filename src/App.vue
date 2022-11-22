<template>
  <summary-card></summary-card>
</template>

<script>
import SummaryCard from "@/components/SummaryCard";

export default {
  name: 'App',
  components: {
    SummaryCard
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Red+Hat+Display:wght@500;700;900&display=swap');
  *, *:visited, *:hover {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
  }

  html {
    background-color: hsla(225, 100%, 94%, 1);
    width: 100vw;
    height: 100vh;
  }

  body {
    width: 100%;
    height: 100%;
    background-image: url("./assets/pattern-background-mobile.svg");
    background-repeat: no-repeat;
    background-position-x: center;
    background-size: 160%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @media screen and (min-width: 650px) {
    body {
      background-image: url("./assets/pattern-background-desktop.svg");
      background-size: 100%;
      background-position-y: -20%;
    }
  }

</style>
