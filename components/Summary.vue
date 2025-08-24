<template>
  <b-card>
    <b-card-title outlined>
      <h5 class="title">Profile Summary</h5>
    </b-card-title>
    <b-card-text>
      <p class="summary-text">
        Results-driven <strong>Senior Front-End Developer</strong> with 6+ years
        of experience architecting and delivering high-performance web
        applications. Proven track record of leading development teams,
        optimizing application performance by 40-60%, and implementing
        enterprise-grade solutions using modern technologies including
        <strong>React 18</strong>, <strong>Vue.js 3</strong>,
        <strong>Next.js 14</strong>
        <strong>Nuxt.js 4</strong>
        , and <strong>TypeScript</strong>.
      </p>
      <p class="summary-text">
        Expert in building scalable, accessible applications with
        <strong>98% Lighthouse accessibility scores</strong> and
        <strong>95+ mobile performance scores</strong>. Skilled in implementing
        secure authentication systems, optimizing SEO strategies resulting in
        <strong>78% search ranking improvements</strong>, and establishing CI/CD
        pipelines that reduce deployment time by <strong>70%</strong>.
      </p>
      <p class="summary-text">
        Passionate about mentoring junior developers, conducting code reviews,
        and driving technical excellence through best practices. Strong advocate
        for performance optimization, accessibility standards, and user-centered
        design principles. Committed to continuous learning and staying current
        with emerging front-end technologies and industry trends.
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
