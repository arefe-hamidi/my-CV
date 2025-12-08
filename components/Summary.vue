<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Profile Summary</h5>
    </b-card-title>
    <b-card-text>
      <p class="summary-text">
        Accomplished <strong>Senior Front-End Developer</strong> with 6+ years
        of expertise in architecting and delivering enterprise-scale web
        applications. Proven track record in leading cross-functional teams and
        driving technical excellence through innovative solutions built with
        modern technologies including <strong>React 19</strong>,
        <strong>Vue.js 3</strong>, <strong>Next.js 15</strong>,
        <strong>Nuxt.js 4</strong>, and <strong>TypeScript</strong>.
      </p>
      <p class="summary-text">
        Specialized in building highly accessible, performant applications that
        meet <strong>excellent Lighthouse accessibility standards</strong> and
        deliver <strong>outstanding mobile performance</strong>. Expert in
        architecting enterprise authentication systems, implementing strategic
        SEO optimizations, and establishing robust CI/CD pipelines that
        streamline development workflows and accelerate time-to-market.
      </p>
      <p class="summary-text">
        Passionate about technical excellence, team mentorship, and continuous
        learning. Strong advocate for performance optimization, accessibility
        standards, and user-centric design principles. Dedicated to staying at
        the forefront of front-end technologies to deliver innovative solutions
        that create meaningful business impact.
      </p>
    </b-card-text>
  </b-card>
</template>

<script>
export default {};
</script>

<style scoped>
.summary-text {
  font-size: 15px;
  line-height: 1.7;
  color: #2c3e50;
  margin-bottom: 16px;
  text-align: justify;
}

.summary-text:last-child {
  margin-bottom: 0;
}

.title {
  color: #2c3e50;
  font-weight: 600;
  margin-bottom: 16px;
}

strong {
  color: #34495e;
  font-weight: 600;
}
</style>
