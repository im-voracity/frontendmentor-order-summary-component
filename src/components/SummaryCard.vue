<template>
  <div class="sub-card">
    <img class="hero" :src="image" alt="">
    <h1 class="heading">Order Summary</h1>
    <p class="description">You can now listen to millions of songs, audiobooks, and podcasts on any device anywhere you
      like!</p>
    <sub-card class="other-card" :icon="icon" plan="Annual Plan" :plan-pricing="59.99"></sub-card>
    <primary-button class="main-button" text="Proceed to Payment"></primary-button>
    <tertiary-button text="Cancel Order"></tertiary-button>
  </div>
</template>

<script>

import image from '../assets/illustration-hero.svg';
import svgIcon from '../assets/icon-music.svg';
import SubCard from "@/components/SubCard";
import PrimaryButton from "@/components/PrimaryButton";
import TertiaryButton from "@/components/TertiaryButton";

export default {
  name: "SummaryCard",
  components: {TertiaryButton, PrimaryButton, SubCard},
  data() {
    return {
      image: image,
      icon: svgIcon
    };
  }
};
</script>

<style scoped>
.sub-card {
  background-color: white;
  width: 327px;
  height: 567px;
  box-shadow: 0 40px 40px -20px hsla(228, 87%, 39%, 0.15);
  border-radius: 20px;
  padding: 0 32px 32px 32px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hero {
  width: 327px;
  height: 160px;
  border-radius: 20px 20px 0 0;
  margin: 0 -32px 32px;
}

.heading {
  font-size: 22px;
  font-family: 'Red Hat Display', sans-serif;
  font-weight: 900;
  line-height: 29px;
  text-align: center;
  margin-bottom: 16px;
  color: hsla(223, 46%, 23%, 1);
}

.description {
  font-size: 15px;
  font-weight: 500;
  font-family: 'Red Hat Display', sans-serif;
  line-height: 25px;
  text-align: center;
  margin-bottom: 24px;
  color: hsla(223, 23%, 55%, 1);
}

.other-card {
  margin-bottom: 24px;
}

.main-button {
  margin-bottom: 24px;
}

@media screen and (min-width: 650px) {
  .sub-card {
    width: 450px;
    height: 697px;
    padding: 0 48px 48px 48px;
  }

  .hero {
    width: 450px;
    height: 220px;
    margin-bottom: 45px;
  }

  .heading {
    font-size: 28px;
    margin-bottom: 17px;
  }

  .description {
    font-size: 16px;
  }

  .other-card {
    margin-bottom: 32px;
  }

  .main-button {
    margin-bottom: 32px;
  }
}

</style>