<script setup>
const certs = [
'Microsoft Azure Fundamentals (AZ-900)',
'ITIL 4 Foundation',
'Certified Automation Engineer Practitioner',
'GI&A Automation Academy Architect L1',
'Connected Manager Certification'
]
</script>

<template>
<section class="section">

<h2>Certifications</h2>

<div class="grid">

<div
v-for="cert in certs"
:key="cert"
class="card"
>
{{ cert }}
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
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}
.card{
padding:20px;
background:#dcfce7;
border-radius:10px;
}
</style>