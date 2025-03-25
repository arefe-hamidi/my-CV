<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Work Experience</h5>
    </b-card-title>
    <b-card-text>
      <div v-for="(work, index) in works" :key="index" class="mt-2">
        <div class="d-flex flex-row">
          <div>
            <h5 class="importent-title">{{ work.jobPosition }}</h5>
          </div>
          <div class="ml-auto">
            <span class="info-detail">
              <img
                src="~/assets/icon/calendar-days-solid.svg"
                class="icon mr-1"
                alt=""
              />{{ work.startDate }} - {{ work.endDate }}
            </span>
          </div>
        </div>
        <div class="info-detail">
          <span>
            {{ work.companyName }} - {{ work.EmploymentType }} (
            {{ work.locationType }})</span
          >
          <!-- <span>
              <img
                src="~/assets/icon/location-dot-solid.svg"
                class="icon"
                alt=""
              />
              {{ work.location }} - {{ work.EmploymentType }} -
              {{ work.locationType }}</span
            > -->
        </div>
        <div
          class="achievement mt-1"
          v-for="(achievement, achIndex) in work.achievements"
          :key="achIndex"
        >
          <img
            src="~/assets/icon/circle-solid.svg"
            class="dot-icon mr-1"
            alt=""
          />
          <span v-html="achievement"></span>
        </div>
      </div>
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  data() {
    return {
      works: [
        {
          jobPosition: "Senior front-end developer",
          companyName: "Ako Rayan",
          EmploymentType: "Full time",
          startDate: "Sep 2023",
          endDate: "Mar 2025",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Developed an efficient solution for handling large file uploads by dividing them into smaller chunks, optimizing the process and reducing upload times.",
            "Designed and developed high-performance, responsive web applications using <strong>React.js</strong> and <strong>TypeScript</strong>, resulting in improved user experience and faster load times.",
            "Delivered consulting services to ensure new websites adhered to accessibility standards, improving usability for all users.",
            "Worked closely with design teams to translate visual designs into efficient and technically sound front-end implementations.",
            "Actively fixed bugs and performed code reviews to improve code quality, utilizing modular architecture patterns within the first month of the project.",
            "Leveraged <strong>React Flow</strong> to build a dynamic and interactive database structure, enhancing the application's data management capabilities.",
          ],
        },
        {
          jobPosition: "Front-end developer",
          companyName: "Start up - Sharif university",
          EmploymentType: "Part time",
          startDate: "Sep 2023",
          endDate: "Jul 2023",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Designed and implemented front-end code using <strong>Vue.js 3</strong> to create highly responsive and user-friendly web applications.",
            "Utilized <strong>Leaflet</strong>, <strong>Vuexy</strong>, <strong>Pinia</strong>, and other modern tools to enhance project functionality and performance.",
          ],
        },
        {
          jobPosition: "Team leader of front-end team",
          companyName: "Nasr Moein Parsayan",
          EmploymentType: "Full time",
          endDate: "Jul 2023",
          startDate: "Apr 2022",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Mentored a team of 4 members, facilitating their professional growth and helping them achieve personal goals.",
            "Worked on projects involving <strong>payment gateway</strong> integration, including payment processing, wallet charging, subscription, and membership plans.",
            "Optimized 15+ key content pages for <strong>SEO</strong> objectives, resulting in a 78% improvement in online search ranking accuracy (utilized <strong>SSR</strong>, <strong>CSR</strong>, <strong>SPA</strong>, <strong>sitemap</strong>, <strong>meta tags</strong>, etc.).",
          ],
        },
        {
          jobPosition: "Senior front-end developer",
          companyName: "Nasr Moein Parsayan",
          EmploymentType: "Full time",
          startDate: "Dec 2020 ",
          endDate: "Apr 2022",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Created modular, responsive templates using modern CSS techniques and JavaScript libraries.",
            "Optimized 18+ applications for maximum speed and scalability.",
            "Utilized <strong>Leaflet</strong>, <strong>CKEditor</strong>, <strong>Vuex</strong>, <strong>Sass</strong>, and other tools in the projects.",
          ],
        },
        {
          jobPosition: "Front-end developer",
          companyName: "Memarenoo",
          EmploymentType: "Freelance",
          startDate: "Jun 2019",
          endDate: "Nov 2020",
          locationType: "On site",
          location: "Gilan Province, Iran",
          achievements: [
            "Designed front-end code using <strong>Vue.js</strong> and <strong>Nuxt.js</strong> to develop responsive websites.",
            "Utilized <strong>D3.js</strong> to create a tree structure for managing menus in the admin panel.",
            "Validated 100% of user input before submitting it to the back-end.",
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.achievement {
  font-size: 14px;
}
</style>
