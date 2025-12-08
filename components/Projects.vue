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
          title: "APC Dev Platform Suite",
          link: "https://apc-dev-platform.azurewebsites.net",
          description:
            "Enterprise development platform with B2B and customer portals built with Next.js 14, featuring role-based authentication and real-time collaboration tools.",
        },
        {
          title: "Drive - HiPixi",
          link: "https://drive.hipixi.com/",
          description:
            "Enterprise file management platform with 2GB chunked uploads, secure sharing, and advanced file organization capabilities.",
        },
        {
          title: "Ako Rayan Website",
          link: "https://akorayan.netlify.app/",
          description:
            "Modern corporate website built with Vue.js 3 and Nuxt.js, featuring responsive design and optimized performance.",
        },
        {
          title: "Charm Database Panel",
          link: "https://charmdb.wingstech.org/",
          description:
            "Dynamic database management interface with React Flow visualization, enabling drag-and-drop relationship modeling.",
        },
        {
          title: "Code Management Platform",
          link: "https://code.wingstech.org/",
          description:
            "Development collaboration platform with version control, project tracking, and team management features.",
        },
        {
          title: "Rayka Transaction Platform",
          link: "http://194.225.78.198/authentication/sign-in",
          description:
            "Financial transaction processing system with secure payment gateway integration and merchant management.",
        },
        {
          title: "Productivity Clock App",
          link: "http://45.92.94.113:4173/login",
          description:
            "Team collaboration tool with time tracking, task management, and project scheduling capabilities.",
        },
        {
          title: "Taksan Industrial Marketplace",
          link: "https://taksaanpre.ir/",
          description:
            "B2B marketplace platform connecting industrial suppliers and buyers with advanced search and transaction features.",
        },
      ],
    };
  },
};
</script>

<style></style>
