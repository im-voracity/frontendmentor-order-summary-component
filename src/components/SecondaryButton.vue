<template>
  <button @click="interaction" class="sb-button">{{text}}</button>
</template>

<script>
export default {
  name: "SecondaryButton",
  props: {
    text: {
      type: String,
      required: true,
      default: 'button'
    }
  },
  methods: {
    interaction() {
      console.log('Here it would display a Modal :D')
    }
  }
};
</script>

<style scoped>
.sb-button {
  font-family: 'Red Hat Display', sans-serif;
  font-size: 13px;
  font-weight: 700;
  border: none;
  background-color: transparent;
  text-decoration-line: underline;
  line-height: 17px;
  color: hsla(245, 75%, 52%, 1);
  transition: 0.3s all ease-in-out;
}

.sb-button:hover {
  color: hsla(245, 83%, 68%, 1);
  cursor: pointer;
}

@media screen and (min-width: 650px) {
  .sb-button {
    font-size: 14px;
  }
}

</style>