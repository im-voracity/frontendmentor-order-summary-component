<template>
  <button class="pm-button">{{text}}</button>
</template>

<script>
export default {
  name: "PrimaryButton",
  props: {
    text: {
      type: String,
      required: true,
      default: 'button'
    }
  }
};
</script>

<style scoped>
  .pm-button {
    width: 100%;
    font-family: 'Red Hat Display', sans-serif;
    font-weight: 900;
    font-size: 15px;
    line-height: 20px;
    padding: 15px 0;
    border: none;
    border-radius: 11px;
    background-color: hsla(245, 75%, 52%, 1);
    color: white;
    box-shadow: 0 20px 20px 0 hsla(245, 75%, 52%, 0.19);
    font-style: normal;
    transition: 0.3s all ease-in-out;
  }

  .pm-button:hover {
    background-color: hsla(245, 83%, 68%, 1);
    cursor: pointer;
  }
</style>