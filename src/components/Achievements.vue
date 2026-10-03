<script setup>
import { ref } from 'vue'

const openIndex = ref(null)

const contributions = [
  {
    title: 'Test Automation',
    subtitle: 'Java, Playwright & Selenium',
    description:
      'Built and supported automated testing solutions using Java, Playwright and Selenium to improve software quality and test coverage.',
    points: [
      'Java-based test automation',
      'Playwright and Selenium WebDriver',
      'Functional and regression automation'
    ]
  },
  {
    title: 'Automation Framework Design',
    subtitle: 'POM, TestNG, JUnit & Maven',
    description:
      'Applied structured automation practices to create maintainable and reusable test solutions.',
    points: [
      'Page Object Model',
      'TestNG and JUnit',
      'Maven-based automation projects'
    ]
  },
  {
    title: 'API Testing',
    subtitle: 'REST API & Postman',
    description:
      'Performed API validation and testing using REST APIs and Postman as part of end-to-end quality assurance.',
    points: [
      'REST API testing',
      'Postman validation',
      'Integration testing'
    ]
  },
  {
    title: 'Quality Assurance',
    subtitle: 'Functional, Regression & UAT',
    description:
      'Supported multiple testing stages to validate application functionality and business requirements.',
    points: [
      'Functional testing',
      'Regression testing',
      'Smoke and sanity testing',
      'UAT support'
    ]
  },
  {
    title: 'Defect Management',
    subtitle: 'Jira & Root Cause Analysis',
    description:
      'Identified, documented and investigated application issues while supporting root cause analysis.',
    points: [
      'Jira defect management',
      'Issue investigation',
      'Root cause analysis'
    ]
  },
  {
    title: 'Agile & CI/CD',
    subtitle: 'Git, Jenkins & Agile/Scrum',
    description:
      'Worked within Agile delivery environments and supported source control and CI/CD practices.',
    points: [
      'Git version control',
      'Jenkins',
      'CI/CD practices',
      'Agile/Scrum'
    ]
  }
]

const toggle = (index) => {
  openIndex.value =
    openIndex.value === index ? null : index
}
</script>

<template>
  <section id="contributions" class="section">

    <div class="section-header">
      <div class="section-badge">
        WHAT I BRING
      </div>

      <h2>
        Key <span>Contributions</span>
      </h2>

      <p>
        Core areas of experience across test automation,
        quality assurance and software delivery.
      </p>
    </div>

    <div class="contribution-grid">

      <article
        v-for="(item, index) in contributions"
        :key="item.title"
        class="contribution-card"
        :class="{ expanded: openIndex === index }"
      >

        <button
          class="card-header"
          type="button"
          @click="toggle(index)"
          :aria-expanded="openIndex === index"
        >

          <div class="card-number">
            {{ String(index + 1).padStart(2, '0') }}
          </div>

          <div class="card-title">
            <h3>{{ item.title }}</h3>
            <span>{{ item.subtitle }}</span>
          </div>

          <div class="expand-icon">
            {{ openIndex === index ? '−' : '+' }}
          </div>

        </button>

        <div
          v-if="openIndex === index"
          class="card-details"
        >
          <p>{{ item.description }}</p>

          <ul>
            <li
              v-for="point in item.points"
              :key="point"
            >
              {{ point }}
            </li>
          </ul>
        </div>

      </article>

    </div>

  </section>
</template>

<style scoped>

.section {
  max-width: 1200px;

  margin: 0 auto;

  padding: 90px 25px;

  background: #ffffff;
}

.section-header {
  max-width: 700px;

  margin: 0 auto 50px;

  text-align: center;
}

.section-badge {
  display: inline-block;

  padding: 8px 16px;

  margin-bottom: 15px;

  border-radius: 25px;

  background: #e8f8f5;

  border: 1px solid #c9eee8;

  color: #078c80;

  font-size: 12px;

  font-weight: 700;

  letter-spacing: 1px;
}

.section-header h2 {
  margin: 0;

  color: #102a43;

  font-size: clamp(2.4rem, 5vw, 3.5rem);

  line-height: 1.1;
}

.section-header h2 span {
  color: #079f91;
}

.section-header p {
  margin: 18px auto 0;

  color: #71869a;

  font-size: 1rem;

  line-height: 1.7;
}

.contribution-grid {
  display: grid;

  grid-template-columns:
    repeat(2, minmax(0, 1fr));

  gap: 16px;
}

.contribution-card {
  overflow: hidden;

  border: 1px solid #e1e9ee;

  border-radius: 15px;

  background: #ffffff;

  transition: 0.25s ease;
}

.contribution-card:hover,
.contribution-card.expanded {
  border-color: #a9ddd7;

  box-shadow:
    0 12px 30px rgba(25, 65, 80, 0.08);
}

.card-header {
  width: 100%;

  display: grid;

  grid-template-columns: 45px 1fr 30px;

  align-items: center;

  gap: 15px;

  padding: 20px;

  border: 0;

  background: transparent;

  text-align: left;
}

.card-number {
  width: 42px;
  height: 42px;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 10px;

  background: #e8f8f5;

  color: #078c80;

  font-size: 12px;

  font-weight: 800;
}

.card-title h3 {
  margin: 0 0 4px;

  color: #102a43;

  font-size: 15px;
}

.card-title span {
  color: #71869a;

  font-size: 12px;
}

.expand-icon {
  color: #078c80;

  font-size: 22px;

  text-align: center;
}

.card-details {
  padding: 0 20px 20px 80px;
}

.card-details p {
  margin: 0 0 12px;

  color: #61788d;

  font-size: 13px;

  line-height: 1.7;
}

.card-details ul {
  margin: 0;

  padding-left: 18px;

  color: #516b79;

  font-size: 12px;

  line-height: 1.8;
}

@media (max-width: 700px) {

  .section {
    padding: 65px 16px;
  }

  .contribution-grid {
    grid-template-columns: 1fr;
  }

  .card-details {
    padding-left: 20px;
  }

}
</style>