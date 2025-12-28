<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Skills</h5>
    </b-card-title>
    <b-card-text>
      <div v-for="(skills, index) in skillsGroup" :key="index" class="mb-4">
        <b-row>
          <b-col cols="4">
            <h5 class="important-title">{{ skills.Title }}</h5>
          </b-col>
          <b-col cols="8">
            <b-row>
              <div
                v-for="(skill, skillIndex) in skills.value"
                :key="skillIndex"
              >
                <div
                  class="d-flex flex-row justify-content-center align-items-center gap-3"
                >
                  <div class="skill-title">
                    {{ skill.title }}
                  </div>
                  <div class="info-detail" v-if="skill.level">
                    ({{ skill.level }})
                  </div>
                  <div
                    v-if="skillIndex < skills.value.length - 1"
                    class="separator"
                  >
                    -
                  </div>
                </div>
              </div>
            </b-row>
          </b-col>
        </b-row>
      </div>
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  data() {
    return {
      skillsGroup: [
        {
          Title: "Core Technologies",
          value: [
            { title: "JavaScript (ES6+)", level: "6+ years" },
            { title: "TypeScript", level: "3+ years" },
            { title: "HTML5 & CSS3", level: "6+ years" },
            { title: "React.js", level: "3+ years" },
            { title: "Vue.js (2 & 3)", level: "6+ years" },
          ],
        },
        {
          Title: "Frameworks & Meta-Frameworks",
          value: [
            { title: "Next.js 15", level: "3+ years" },
            { title: "React 19", level: "3+ years" },
            { title: "Nuxt.js 4", level: "6+ years" },
            { title: "Remix", level: "6 months" },
          ],
        },
        {
          Title: "State Management & Data Flow",
          value: [
            { title: "TanStack Query (React Query)", level: "1+ year" },
            { title: "Zustand", level: "2+ years" },
            { title: "Redux Toolkit", level: "3+ years" },
            { title: "Vuex", level: "6+ years" },
            { title: "Pinia", level: "1+ year" },
          ],
        },
        {
          Title: "UI/UX & Styling",
          value: [
            { title: "Tailwind CSS", level: "3+ years" },
            { title: "Shadcn/UI", level: "1+ year" },
            { title: "Material Design", level: "6+ years" },
            { title: "Sass/SCSS", level: "6+ years" },
            { title: "Bootstrap", level: "6+ years" },
          ],
        },
        {
          Title: "Specialized Libraries & Tools",
          value: [
            { title: "Auth.js (NextAuth.js)", level: "1+ year" },
            { title: "Azure AD B2C", level: "1+ year" },
            { title: "React Flow", level: "1+ year" },
            { title: "D3.js", level: "2+ years" },
            { title: "Leaflet.js", level: "2+ years" },
            { title: "CKEditor", level: "3+ years" },
            { title: "Internationalization (i18n)", level: "2+ years" },
          ],
        },
        {
          Title: "Development & DevOps",
          value: [
            { title: "Git & GitHub", level: "6+ years" },
            { title: "Azure DevOps", level: "1+ year" },
            { title: "CI/CD Pipelines", level: "3+ years" },
            { title: "Docker", level: "2+ years" },
            { title: "Webpack & Vite", level: "4+ years" },
            { title: "proxyFetch", level: "1+ year" },
          ],
        },
        {
          Title: "Testing & Quality Assurance",
          value: [
            { title: "Vitest", level: "1+ year" },
            { title: "React Testing Library", level: "1+ year" },
            { title: "Unit Testing", level: "2+ years" },
            { title: "Test-Driven Development (TDD)", level: "1+ year" },
          ],
        },
        {
          Title: "Performance & Optimization",
          value: [
            { title: "Lighthouse Auditing", level: "3+ years" },
            { title: "SEO Optimization", level: "4+ years" },
            { title: "Performance Optimization", level: "5+ years" },
            { title: "Bundle Optimization", level: "4+ years" },
            { title: "SSR/SSG Optimization", level: "3+ years" },
          ],
        },
        {
          Title: "Languages & Communication",
          value: [
            { title: "English", level: "Professional" },
            { title: "Persian", level: "Native" },
          ],
        },
        {
          Title: "Architecture & Patterns",
          value: [
            { title: "Fractal Modular Architecture" },
            { title: "Component-Based Architecture" },
            { title: "Design Patterns" },
            { title: "API Design & Integration" },
            { title: "Error Handling Strategies" },
          ],
        },
        {
          Title: "Leadership & Soft Skills",
          value: [
            { title: "Team Leadership" },
            { title: "Technical Mentoring" },
            { title: "Code Review & Best Practices" },
            { title: "Agile/Scrum Methodologies" },
            { title: "Project Management" },
            { title: "Technical Documentation" },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.important-title {
  color: #2c3e50;
  font-weight: 600;
  font-size: 16px;
  margin-bottom: 8px;
}

.skill-title {
  font-weight: 500;
  color: #34495e;
}

.info-detail {
  color: #6c757d;
  font-size: 13px;
  font-style: italic;
}

.separator {
  color: #34495e;
  font-weight: 300;
}

.title {
  color: #2c3e50;
  font-weight: 600;
}
</style>
