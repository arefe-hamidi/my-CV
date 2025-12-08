<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Work Experience</h5>
    </b-card-title>
    <b-card-text>
      <div v-for="(work, index) in works" :key="index" class="mt-3">
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
        </div>
        <div
          class="achievement mt-2"
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
          jobPosition: "Senior Front-End Developer",
          companyName: "Desinno Soft",
          EmploymentType: "Full time",
          startDate: "Jul 2025",
          endDate: "Present",
          locationType: "Remote",
          location: "Dubai, United Arab Emirates",
          achievements: [
            "Led development of modern, scalable web applications using <strong>Next.js 15</strong> and <strong>React 19</strong>, achieving significantly faster page load times through optimized SSR and static generation strategies.",
            "Implemented enterprise-grade authentication using <strong>Auth.js (NextAuth.js)</strong> with role-based access control, significantly reducing security incidents and improving user session management.",
            "Architected state management solutions using <strong>Zustand</strong> , resulting in substantial reduction in API calls and improved data consistency across the application.",
            "Built responsive, accessible UI components using <strong>Tailwind CSS</strong> and <strong>Shadcn/UI</strong>, maintaining high Lighthouse accessibility scores and excellent mobile performance.",
            "Established CI/CD pipelines using <strong>Microsoft Azure DevOps</strong>, significantly reducing deployment time and implementing automated testing with comprehensive code coverage.",
          ],
        },
        {
          jobPosition: "Senior Front-End Developer",
          companyName: "Ako Rayan",
          EmploymentType: "Full time",
          startDate: "Sep 2023",
          endDate: "Mar 2025",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Developed a chunked file upload system handling files up to 2GB, significantly reducing upload failures and improving user experience for large file transfers.",
            "Built high-performance web applications using <strong>React.js</strong> and <strong>TypeScript</strong>, achieving substantial improvement in bundle size and faster rendering through code splitting and lazy loading.",
            "Implemented <strong>React Flow</strong> for dynamic database structure visualization, enabling users to create and modify complex data relationships with drag-and-drop functionality.",
            "Conducted comprehensive accessibility audits and implemented WCAG 2.1 AA compliance, improving usability for users with disabilities and achieving full keyboard navigation support.",
            "Established code review processes and modular architecture patterns, reducing bug reports and improving code maintainability across the team.",
          ],
        },
        {
          jobPosition: "Front-End Developer",
          companyName: "Startup - Sharif University",
          EmploymentType: "Part time",
          startDate: "Sep 2023",
          endDate: "Jul 2023",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Developed responsive web applications using <strong>Vue.js 3</strong> with Composition API, significantly improving component reusability and reducing development time.",
            "Integrated <strong>Leaflet</strong> for interactive mapping features and <strong>Pinia</strong> for state management, creating seamless user experiences for location-based services.",
            "Utilized <strong>Vuexy</strong> design system to maintain consistent UI/UX patterns across multiple applications.",
          ],
        },
        {
          jobPosition: "Team Leader - Front-End Development",
          companyName: "Nasr Moein Parsayan",
          EmploymentType: "Full time",
          endDate: "Jul 2023",
          startDate: "Apr 2022",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Led and mentored a team of 4 front-end developers, significantly improving team productivity and reducing project delivery time through effective code reviews and pair programming.",
            "Architected and implemented payment gateway integrations including Stripe and PayPal, processing over $2M in transactions with high success rate and comprehensive error handling.",
            "Optimized 15+ key pages for SEO using <strong>SSR</strong>, <strong>CSR</strong>, and <strong>SPA</strong> strategies, resulting in substantial improvement in search rankings and significant increase in organic traffic.",
            "Implemented automated testing strategies and CI/CD pipelines, reducing production bugs and deployment time.",
          ],
        },
        {
          jobPosition: "Senior Front-End Developer",
          companyName: "Nasr Moein Parsayan",
          EmploymentType: "Full time",
          startDate: "Dec 2020",
          endDate: "Apr 2022",
          locationType: "Remote",
          location: "Tehran, Tehran Province, Iran",
          achievements: [
            "Developed modular, responsive templates using modern CSS techniques and JavaScript libraries, significantly improving page load speed and mobile responsiveness scores.",
            "Optimized 18+ applications for maximum performance and scalability, implementing lazy loading and code splitting strategies that substantially reduced initial bundle size.",
            "Integrated <strong>Leaflet</strong> for interactive maps, <strong>CKEditor</strong> for rich text editing, and <strong>Vuex</strong> for state management, enhancing user experience across multiple applications.",
            "Implemented <strong>Sass</strong> architecture and CSS custom properties, reducing CSS bundle size and improving maintainability across the codebase.",
          ],
        },
        {
          jobPosition: "Front-End Developer",
          companyName: "Memarenoo",
          EmploymentType: "Freelance",
          startDate: "Jun 2019",
          endDate: "Nov 2020",
          locationType: "On site",
          location: "Gilan Province, Iran",
          achievements: [
            "Built responsive websites using <strong>Vue.js</strong> and <strong>Nuxt.js</strong>, implementing SSR for improved SEO and faster initial page loads.",
            "Developed interactive admin panel using <strong>D3.js</strong> for dynamic menu management, enabling drag-and-drop functionality for complex hierarchical structures.",
            "Implemented comprehensive client-side validation with complete input sanitization, significantly reducing server-side errors and improving data integrity.",
            "Collaborated with design and backend teams to ensure seamless integration and optimal user experience across all touchpoints.",
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
  line-height: 1.6;
  margin-bottom: 8px;
}

.importent-title {
  color: #2c3e50;
  font-weight: 600;
  margin-bottom: 4px;
}

.info-detail {
  color: #6c757d;
  font-size: 14px;
  margin-bottom: 8px;
}
</style>
