<template>
  <button class="tb-button">{{text}}</button>
</template>

<script>
export default {
  name: "TertiaryButton",
  props: {
    text: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
.tb-button {
  font-family: 'Red Hat Display', sans-serif;
  font-style: normal;
  font-weight: 900;
  font-size: 15px;
  line-height: 20px;
  color: hsla(224, 23%, 55%, 1);
  border: none;
  background-color: transparent;
  transition: 0.3s all ease-in-out;
}

.tb-button:hover {
  color: hsla(223, 47%, 23%, 1);
  cursor: pointer;
}
</style>