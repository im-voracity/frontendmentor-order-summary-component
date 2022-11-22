<template>
  <div class="mini-card">
    <svg class="music-icon" xmlns="http://www.w3.org/2000/svg" width="48" height="48">
      <g fill="none" fill-rule="evenodd">
        <circle cx="24" cy="24" r="24" fill="#DFE6FB"/>
        <path fill="#717FA6" fill-rule="nonzero"
              d="M32.574 15.198a.81.81 0 00-.646-.19L20.581 16.63a.81.81 0 00-.696.803V26.934a3.232 3.232 0 00-1.632-.44A3.257 3.257 0 0015 29.747 3.257 3.257 0 0018.253 33a3.257 3.257 0 003.253-3.253v-8.37l9.726-1.39v5.327a3.232 3.232 0 00-1.631-.441 3.257 3.257 0 00-3.254 3.253 3.257 3.257 0 003.254 3.253 3.257 3.257 0 003.253-3.253V15.81a.81.81 0 00-.28-.613z"/>
      </g>
    </svg>
    <div class="plan-details">
      <p class="plan-name">{{plan}}</p>
      <p class="plan-pricing">${{planPricing}}/year</p>
    </div>
    <secondary-button text="change"></secondary-button>
  </div>
</template>

<script>
import SecondaryButton from "@/components/SecondaryButton";

export default {
  name: "SubCard",
  components: {SecondaryButton},
  props: {
    plan: {
      type: String,
      required: true
    },
    planPricing: {
      type: Number,
      required: true
    }
  }
};
</script>

<style scoped>
.mini-card {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  background-color: hsla(228, 100%, 99%, 1);
  width: 100%;
  height: 279px;
  border-radius: 11px;
  padding: 16px;
}

.music-icon {
  margin-right: 20px;
}

.plan-details {
  margin-right: 40px;
  max-width: 81px;
  font-family: 'Red Hat Display', sans-serif;
  line-height: 19px;
}

.plan-name {
  font-size: 13px;
  font-weight: 900;
  color: hsla(223, 46%, 23%, 1);
}

.plan-pricing {
  font-size: 14px;
  font-weight: 500;
  color: hsla(224, 23%, 55%, 1);
}

@media screen and (min-width: 650px) {
  .mini-card {
    height: 98px;
    padding: 25px;
  }

  .plan-details {
    margin-right: 90px;
  }

  .plan-name {
    font-size: 16px;
    min-width: 118px;
  }

  .plan-pricing {
    font-size: 16px;
  }
}

</style>