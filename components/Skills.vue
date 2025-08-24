<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Skills</h5>
    </b-card-title>
    <b-card-text>
      <div v-for="(skills, index) in skillsGroup" :key="index" class="mb-4">
        <b-row>
          <b-col cols="4">
            <h5 class="importent-title">{{ skills.Title }}</h5>
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
          Title: "Programming Languages",
          value: [
            { title: "JavaScript (ES6+)", level: "6+ years" },
            { title: "TypeScript", level: "3+ years" },
            { title: "HTML5", level: "6+ years" },
            { title: "CSS3", level: "6+ years" },
          ],
        },
        {
          Title: "Frontend Frameworks",
          value: [
            { title: "React.js", level: "3+ years" },
            { title: "Vue.js (2 & 3)", level: "6+ years" },
            { title: "Next.js", level: "3+ years" },
            { title: "Nuxt.js", level: "6+ years" },
            { title: "Remix", level: "6 months" },
          ],
        },
        {
          Title: "State Management",
          value: [
            { title: "Redux", level: "3+ years" },
            { title: "Vuex", level: "6+ years" },
            { title: "Pinia", level: "1+ year" },
            { title: "Zustand", level: "2+ years" },
          ],
        },
        {
          Title: "UI Libraries & Design Systems",
          value: [
            { title: "Tailwind CSS", level: "3+ years" },
            { title: "Bootstrap", level: "6+ years" },
            { title: "Vuetify", level: "6+ years" },
            { title: "Shadcn/UI", level: "3+ months" },
            { title: "Material Design", level: "6+ years" },
            { title: "Sass/SCSS", level: "6+ years" },
          ],
        },
        {
          Title: "Development Tools",
          value: [
            { title: "Git & GitHub", level: "6+ years" },
            { title: "Storybook", level: "2+ years" },
            { title: "Webpack", level: "4+ years" },
            { title: "Vite", level: "2+ years" },
            { title: "ESLint & Prettier", level: "4+ years" },
          ],
        },
        {
          Title: "Specialized Libraries",
          value: [
            { title: "Leaflet.js", level: "2+ years" },
            { title: "D3.js", level: "2+ years" },
            { title: "React Flow", level: "1+ year" },
            { title: "CKEditor", level: "3+ years" },
            { title: "Auth.js (NextAuth)", level: "3+ months" },
          ],
        },
        {
          Title: "DevOps & Deployment",
          value: [
            { title: "Azure DevOps", level: "3+ months" },
            { title: "CI/CD Pipelines", level: "3+ years" },
            { title: "Docker", level: "2+ years" },
          ],
        },
        {
          Title: "Performance & SEO",
          value: [
            { title: "SEO Optimization", level: "4+ years" },
            { title: "Lighthouse Auditing", level: "3+ years" },
            { title: "Performance Optimization", level: "5+ years" },
          ],
        },
        {
          Title: "Languages",
          value: [
            { title: "English", level: "Intermediate" },
            { title: "Persian", level: "Native" },
          ],
        },
        {
          Title: "Soft Skills",
          value: [
            { title: "Team Leadership" },
            { title: "Problem Solving" },
            { title: "Project Management" },
            { title: "Code Review" },
            { title: "Mentoring" },
            { title: "Agile/Scrum" },
            { title: "Technical Documentation" },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.importent-title {
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
  color: #dee2e6;
  font-weight: 300;
}

.title {
  color: #2c3e50;
  font-weight: 600;
}
</style>
