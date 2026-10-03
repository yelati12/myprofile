<script setup>
import { ref } from 'vue'

const openIndex = ref(0)

const experiences = [
  {
    company: 'Amazon Development India',
    role: 'Software Engineer',
    focus: 'Test Automation & Quality Assurance',
    tags: ['Java', 'Playwright', 'Selenium'],
    responsibilities: [
      'Worked on software test automation using Java, Playwright and Selenium.',
      'Applied Page Object Model practices for maintainable automation.',
      'Performed functional, regression, smoke and sanity testing.',
      'Supported integration testing and UAT activities.',
      'Performed REST API testing using Postman.',
      'Logged and tracked defects using Jira.',
      'Supported root cause analysis for application issues.',
      'Worked within Agile/Scrum development environments.',
      'Used Git, Jenkins and CI/CD practices.'
    ]
  },
  {
    company: 'Knoah Solutions',
    role: 'Software Engineer',
    focus: 'Healthcare Application Testing & Automation',
    tags: ['Testing', 'Automation', 'Healthcare'],
    responsibilities: [
      'Performed testing of healthcare applications.',
      'Executed functional, regression, smoke and sanity testing.',
      'Supported integration testing activities.',
      'Developed test automation using Java.',
      'Applied Page Object Model practices.',
      'Performed REST API testing using Postman.',
      'Managed defects through Jira.',
      'Supported root cause analysis.',
      'Worked in an Agile/Scrum environment.'
    ]
  }
]

const toggle = (index) => {
  openIndex.value =
    openIndex.value === index ? null : index
}
</script>

<template>
  <section id="experience" class="section">

    <div class="section-header">

      <div class="section-badge">
        CAREER JOURNEY
      </div>

      <h2>
        Professional <span>Experience</span>
      </h2>

      <p>
        Experience across software testing, automation,
        technical support and quality assurance.
      </p>

    </div>

    <div class="timeline">

      <article
        v-for="(item, index) in experiences"
        :key="item.company"
        class="experience-card"
        :class="{ expanded: openIndex === index }"
      >

        <div class="timeline-marker">
          {{ index + 1 }}
        </div>

        <button
          class="experience-header"
          type="button"
          @click="toggle(index)"
          :aria-expanded="openIndex === index"
        >

          <div>
            <h3>{{ item.company }}</h3>

            <h4>{{ item.role }}</h4>

            <p>{{ item.focus }}</p>

            <div class="tags">
              <span
                v-for="tag in item.tags"
                :key="tag"
              >
                {{ tag }}
              </span>
            </div>
          </div>

          <div class="expand">
            {{ openIndex === index ? '−' : '+' }}
          </div>

        </button>

        <div
          v-if="openIndex === index"
          class="responsibilities"
        >

          <h5>Key Responsibilities</h5>

          <ul>
            <li
              v-for="responsibility in item.responsibilities"
              :key="responsibility"
            >
              {{ responsibility }}
            </li>
          </ul>

        </div>

      </article>

    </div>

  </section>
</template>

<style scoped>

.section {
  max-width: 1100px;

  margin: 0 auto;

  padding: 90px 25px;

  background: #ffffff;
}

.section-header {
  text-align: center;

  margin-bottom: 50px;
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
  max-width: 650px;

  margin: 18px auto 0;

  color: #71869a;

  line-height: 1.7;
}

.timeline {
  position: relative;

  display: flex;

  flex-direction: column;

  gap: 20px;
}

.timeline::before {
  content: "";

  position: absolute;

  left: 22px;

  top: 30px;
  bottom: 30px;

  width: 1px;

  background: #cceee8;
}

.experience-card {
  position: relative;

  margin-left: 55px;

  border: 1px solid #e1e9ee;

  border-radius: 16px;

  background: white;

  transition: 0.25s ease;
}

.experience-card:hover,
.experience-card.expanded {
  border-color: #a9ddd7;

  box-shadow:
    0 12px 30px rgba(25, 65, 80, 0.08);
}

.timeline-marker {
  position: absolute;

  left: -55px;
  top: 25px;

  width: 45px;
  height: 45px;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 50%;

  background: #e8f8f5;

  border: 1px solid #c9eee8;

  color: #078c80;

  font-size: 13px;

  font-weight: 800;
}

.experience-header {
  width: 100%;

  display: grid;

  grid-template-columns: 1fr 35px;

  gap: 20px;

  padding: 25px;

  border: 0;

  background: transparent;

  text-align: left;
}

.experience-header h3 {
  margin: 0 0 5px;

  color: #102a43;

  font-size: 18px;
}

.experience-header h4 {
  margin: 0 0 5px;

  color: #079f91;

  font-size: 14px;
}

.experience-header p {
  margin: 0 0 15px;

  color: #71869a;

  font-size: 13px;
}

.tags {
  display: flex;

  flex-wrap: wrap;

  gap: 7px;
}

.tags span {
  padding: 5px 9px;

  border-radius: 6px;

  background: #f3f8f8;

  color: #496b73;

  font-size: 11px;

  font-weight: 600;
}

.expand {
  color: #078c80;

  font-size: 22px;

  text-align: center;
}

.responsibilities {
  padding: 0 25px 25px;

  border-top: 1px solid #edf1f3;
}

.responsibilities h5 {
  margin: 20px 0 10px;

  color: #102a43;

  font-size: 13px;
}

.responsibilities ul {
  margin: 0;

  padding-left: 18px;

  color: #61788d;

  font-size: 13px;

  line-height: 1.8;
}

@media (max-width: 650px) {

  .section {
    padding: 65px 16px;
  }

  .timeline::before {
    display: none;
  }

  .experience-card {
    margin-left: 0;
  }

  .timeline-marker {
    display: none;
  }

  .experience-header {
    padding: 20px;
  }

  .responsibilities {
    padding: 0 20px 20px;
  }

}
</style>