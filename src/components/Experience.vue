<script setup>
import { ref } from 'vue'

const openIndex = ref(null)

const toggleJob = (index) => {
  openIndex.value = openIndex.value === index ? null : index
}

const jobs = [
  {
    company: 'Capgemini UK — Barclays',
    role: 'Automation Engineer',
    period: 'Apr 2025 – Present',
    responsibilities: [
      'Delivering end-to-end QA and test automation across Retail Banking and Fraud Detection systems within Agile/Scrum SDLC.',
      'Built a scalable POM-based Playwright (Java) automation framework from scratch.',
      'Automated authentication, fraud alert journeys, account management, and banking workflows.',
      'Delivered UI and REST API automation using Playwright with parallel execution and retry mechanisms.',
      'Performed ETL, SQL, database, and data validation testing.',
      'Integrated automation suites with Azure DevOps, Jenkins and GitLab CI/CD pipelines.',
      'Captured screenshots, videos, and trace files to accelerate defect resolution.'
    ]
  },
  {
    company: 'Capgemini India — Co-operative Bank',
    role: 'Automation Test Engineer',
    period: 'May 2024 – Apr 2025',
    responsibilities: [
      'Led and mentored a QA automation team of 4–5 engineers.',
      'Led mobile automation using Appium, Xcode, Android Studio and BrowserStack.',
      'Developed Selenium Serenity BDD automation framework.',
      'Reduced test flakiness and improved execution efficiency.',
      'Collaborated with development teams to improve application stability.'
    ]
  },
  {
    company: 'Capgemini — ABN AMRO Netherlands',
    role: 'Technical Lead | Automation Test Engineer',
    period: 'Jan 2021 – May 2024',
    responsibilities: [
      'Delivered automation across Multi-Currency, Insurance, Mortgage and Retail Banking domains.',
      'Built Hybrid Selenium-Cucumber BDD framework with TestNG.',
      'Developed REST API automation framework and used Postman for API validation.',
      'Implemented Selenium Grid for parallel execution.',
      'Integrated automation with GitLab CI/CD pipelines.',
      'Led test estimation, planning, strategy and reporting activities.',
      'Performed Appium mobile testing using Sauce Labs.'
    ]
  },
  {
    company: 'Capgemini India — GE Healthcare',
    role: 'Automation Test Engineer',
    period: 'Aug 2017 – Jan 2021',
    responsibilities: [
      'Validated PET-CT medical imaging workflows and regulatory compliance.',
      'Implemented Hybrid TestNG automation framework using POM.',
      'Participated in Agile ceremonies and sprint delivery.',
      'Performed Functional, Regression, Smoke, Performance and Load Testing.',
      'Implemented Data-Driven Testing using Apache POI and TestNG.'
    ]
  },
  {
    company: 'Sutherland Global Services — Siemens',
    role: 'Software Engineer (Test)',
    period: 'Jan 2012 – Aug 2017',
    responsibilities: [
      'Delivered testing across Insurance and Healthcare applications.',
      'Developed Selenium WebDriver automation using TestNG and Maven.',
      'Performed requirement analysis and manual testing.',
      'Contributed to test strategy, defect management and Agile delivery.'
    ]
  }
]
</script>

<template>
  <section class="experience-section">
    <h2>Professional Experience</h2>
    <p class="subtitle">
      10+ Years of Quality Engineering, Test Automation and Technical Leadership Experience
    </p>

    <div
      v-for="(job, index) in jobs"
      :key="index"
      class="job-card"
    >
      <div
        class="job-header"
        @click="toggleJob(index)"
      >
        <div>
          <h3>{{ job.company }}</h3>
          <h4>{{ job.role }}</h4>
          <p>{{ job.period }}</p>
        </div>

        <div class="arrow">
          {{ openIndex === index ? '▲' : '▼' }}
        </div>
      </div>

      <transition name="fade">
        <div
          v-if="openIndex === index"
          class="job-details"
        >
          <ul>
            <li
              v-for="(item, idx) in job.responsibilities"
              :key="idx"
            >
              {{ item }}
            </li>
          </ul>
        </div>
      </transition>
    </div>
  </section>
</template>

<style scoped>
.experience-section {
  max-width: 1100px;
  margin: auto;
  padding: 80px 20px;
}

.experience-section h2 {
  text-align: center;
  font-size: 2.5rem;
  color: #111827;
  margin-bottom: 10px;
}

.subtitle {
  text-align: center;
  color: #6b7280;
  margin-bottom: 50px;
}

.job-card {
  background: white;
  border-radius: 16px;
  margin-bottom: 20px;
  border-left: 5px solid #14b8a6;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
  overflow: hidden;
}

.job-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 25px;
  cursor: pointer;
}

.job-header h3 {
  color: #111827;
  margin-bottom: 4px;
}

.job-header h4 {
  color: #14b8a6;
  margin-bottom: 6px;
}

.job-header p {
  color: #6b7280;
}

.arrow {
  font-size: 1.4rem;
  color: #14b8a6;
  font-weight: bold;
}

.job-details {
  padding: 0 25px 25px;
}

.job-details ul {
  padding-left: 20px;
}

.job-details li {
  margin-bottom: 12px;
  color: #374151;
  line-height: 1.7;
}

.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  max-height: 0;
}

.fade-enter-to,
.fade-leave-from {
  opacity: 1;
  max-height: 800px;
}

@media (max-width: 768px) {
  .job-header {
    flex-direction: column;
    align-items: flex-start;
  }

  .arrow {
    margin-top: 10px;
  }
}
</style>