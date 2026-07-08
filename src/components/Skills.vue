<script setup>
const skills = [
'Playwright',
'Selenium',
'Appium',
'REST Assured',
'Postman',
'Karate',
'Java',
'JavaScript',
'Azure',
'Azure DevOps',
'GitLab CI/CD',
'Jenkins',
'Docker',
'TestNG',
'BDD',
'Cucumber',
'Serenity',
'POM'
]
</script>

<template>
<section class="section">

<h2>Technical Skills</h2>

<div class="grid">
  <div
    v-for="skill in skills"
    :key="skill"
    class="card"
  >
    {{ skill }}
  </div>
</div>

</section>
</template>

<style scoped>
.section{
padding:80px;
}
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:20px;
}
.card{
padding:20px;
background:#eef2ff;
border-radius:10px;
text-align:center;
}
</style>