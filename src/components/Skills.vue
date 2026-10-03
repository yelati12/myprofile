<script setup>
import { ref } from 'vue'

const openIndex = ref(null)

const skillGroups = [
  {
    title: 'Automation Testing',
    description: 'Web automation tools and test framework practices.',
    skills: [
      'Playwright',
      'Selenium WebDriver',
      'TestNG',
      'JUnit',
      'Page Object Model'
    ]
  },
  {
    title: 'Programming',
    description: 'Programming language used for automation development.',
    skills: [
      'Java'
    ]
  },
  {
    title: 'API Testing',
    description: 'API validation and integration testing.',
    skills: [
      'REST API',
      'Postman'
    ]
  },
  {
    title: 'BDD & Frameworks',
    description: 'Framework and development practices.',
    skills: [
      'Cucumber',
      'BDD',
      'Maven'
    ]
  },
  {
    title: 'DevOps & Version Control',
    description: 'Tools supporting source control and delivery.',
    skills: [
      'Git',
      'Jenkins',
      'CI/CD'
    ]
  },
  {
    title: 'QA & Delivery',
    description: 'Testing methodologies and quality practices.',
    skills: [
      'Functional Testing',
      'Regression Testing',
      'Smoke Testing',
      'Sanity Testing',
      'Integration Testing',
      'UAT',
      'Jira',
      'Root Cause Analysis',
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
  <section id="skills" class="section">

    <div class="section-header">

      <div class="section-badge">
        TECHNICAL EXPERTISE
      </div>

      <h2>
        Technical <span>Skills</span>
      </h2>

      <p>
        Tools, technologies and testing practices used across
        software quality assurance and automation.
      </p>

    </div>

    <div class="skills-grid">

      <article
        v-for="(group, index) in skillGroups"
        :key="group.title"
        class="skill-card"
        :class="{ expanded: openIndex === index }"
      >

        <button
          class="skill-header"
          type="button"
          @click="toggle(index)"
          :aria-expanded="openIndex === index"
        >

          <div class="skill-icon">
            {{ String(index + 1).padStart(2, '0') }}
          </div>

          <div class="skill-title">
            <h3>{{ group.title }}</h3>
            <p>{{ group.description }}</p>
          </div>

          <span class="arrow">
            {{ openIndex === index ? '−' : '+' }}
          </span>

        </button>

        <div class="skill-tags">

          <span
            v-for="skill in (
              openIndex === index
                ? group.skills
                : group.skills.slice(0, 3)
            )"
            :key="skill"
          >
            {{ skill }}
          </span>

          <span
            v-if="openIndex !== index && group.skills.length > 3"
            class="more"
          >
            +{{ group.skills.length - 3 }}
          </span>

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
}

.section-header h2 span {
  color: #079f91;
}

.section-header p {
  margin: 18px auto 0;

  color: #71869a;

  line-height: 1.7;
}

.skills-grid {
  display: grid;

  grid-template-columns:
    repeat(2, minmax(0, 1fr));

  gap: 16px;
}

.skill-card {
  padding: 20px;

  border: 1px solid #e1e9ee;

  border-radius: 15px;

  background: white;

  transition: 0.25s ease;
}

.skill-card:hover,
.skill-card.expanded {
  border-color: #a9ddd7;

  box-shadow:
    0 12px 30px rgba(25, 65, 80, 0.08);
}

.skill-header {
  width: 100%;

  display: grid;

  grid-template-columns: 45px 1fr 25px;

  align-items: center;

  gap: 14px;

  padding: 0;

  border: 0;

  background: transparent;

  text-align: left;
}

.skill-icon {
  width: 42px;
  height: 42px;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 10px;

  background: #e8f8f5;

  color: #078c80;

  font-size: 11px;

  font-weight: 800;
}

.skill-title h3 {
  margin: 0 0 4px;

  color: #102a43;

  font-size: 15px;
}

.skill-title p {
  margin: 0;

  color: #8799a6;

  font-size: 11px;
}

.arrow {
  color: #078c80;

  font-size: 21px;

  text-align: center;
}

.skill-tags {
  display: flex;

  flex-wrap: wrap;

  gap: 7px;

  margin-top: 17px;
}

.skill-tags span {
  padding: 6px 9px;

  border-radius: 6px;

  background: #f3f8f8;

  color: #496b73;

  font-size: 11px;

  font-weight: 600;
}

.skill-tags .more {
  background: #e8f8f5;

  color: #078c80;
}

@media (max-width: 700px) {

  .section {
    padding: 65px 16px;
  }

  .skills-grid {
    grid-template-columns: 1fr;
  }

}
</style>