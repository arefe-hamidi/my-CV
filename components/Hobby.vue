<template>
  <div>
    <b-card>
      <b-card-title outlined>
        <h5 class="title">Hobby</h5>
      </b-card-title>
      <b-card-text>
        <div v-for="(hooby, index) in hobbies" :key="index">
          <img
            src="~/assets/icon/circle-solid.svg"
            class="dot-icon mr-1"
            alt=""
          />{{ hooby }}
        </div>
      </b-card-text>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hobbies: [
        "Nature photography and outdoor activities",
        "Traditional art appreciation and creative writing",
        "Digital painting and visual design",
        "Cultural exploration through travel and culinary experiences",
      ],
    };
  },
};
</script>

<style></style>
