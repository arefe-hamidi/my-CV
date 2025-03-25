<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Skills</h5>
    </b-card-title>
    <b-card-text>
      <div v-for="(skills, index) in skillsGroup" :key="index">
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
                  <div>
                    {{ skill.title }}
                  </div>
                  <div class="info-detail" v-if="skill.level">
                    ({{ skill.level }})
                  </div>
                  <div v-if="skillIndex < skills.value.length - 1">-</div>
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
          Title: "Programming languages",
          value: [
            { title: "JavaScript", level: "6 years" },
            { title: "TypeScript", level: "3 years" },
          ],
        },
        {
          Title: "Libraries",
          value: [
            { title: "React", level: "3 years" },
            { title: "Redux", level: "3 years" },
            { title: "Vuex", level: "6 years" },
            { title: "Pinia", level: "1 year" },
            { title: "Leaflet", level: "1 year" },
          ],
        },
        {
          Title: "Frameworks",
          value: [
            { title: "Vue js (2 & 3)", level: "6 years" },
            { title: "Next js", level: "3 years" },
            { title: "Nuxt js", level: "6 years" },
            { title: "Vuetify", level: "6 years" },
            { title: "Remix", level: "6 months" },
          ],
        },
        {
          Title: "Other skills",
          value: [
            { title: "SEO" },
            { title: "HTML" },
            { title: "CSS" },
            { title: "Sass " },
            { title: "Bootstrap" },
            { title: "Tailwind" },
            { title: "Material Design " },
            { title: "Git " },
            { title: "Storybook" },
          ],
        },
        {
          Title: "Languages",
          value: [
            { title: "English", level: " Intermediate" },
            { title: "Persian ", level: "Native" },
          ],
        },
        {
          Title: "Soft skills",
          value: [
            { title: "Teamwork" },
            { title: "Problem solving " },
            {
              title: "project management",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style></style>
