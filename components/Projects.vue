<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Projects</h5>
    </b-card-title>
    <b-card-text>
      <div v-for="(proj, index) in projects" :key="index">
        <img
          src="~/assets/icon/circle-solid.svg"
          class="dot-icon mr-1"
          alt=""
        />
        <a :href="proj.link">
          <span class="title">{{ proj.title }}</span>
        </a>

        <span class="info-detail" v-if="proj.description"
          >( {{ proj.description }} )</span
        >
      </div>
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Drive - HiPixi ",
          link: "https://drive.hipixi.com/",
          description:
            "An enterprise platform for secure file uploading, management, and sharing.",
        },
        {
          title: "Ako Rayan website",
          link: "https://akorayan.netlify.app/",
          description:
            "A modern, responsive website turning ideas into real-world applications.",
        },
        {
          title: "Charm db panel",
          link: "https://charmdb.wingstech.org/",
          description:
            "A flexible database management panel with seamless collaboration features.",
        },
        {
          title: "Code in One panel",
          link: "https://code.wingstech.org/",
          description:
            "A development panel optimizing coding efficiency and project management.",
        },
        {
          title: "Rayka Txp",
          link: "http://194.225.78.198/authentication/sign-in",
          description:
            "A financial platform for transaction processing and merchant tax calculations.",
        },
        {
          title: "Clock App",
          link: "http://45.92.94.113:4173/login",
          description:
            "A productivity tool for time management, task scheduling, and team collaboration.",
        },
        {
          title: "Taksan",
          link: "https://taksaanpre.ir/",
          description:
            "An industrial marketplace connecting suppliers and buyers for seamless transactions.",
        },
      ],
    };
  },
};
</script>

<style></style>
