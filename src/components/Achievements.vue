<script setup>
import { ref } from 'vue'

const openIndex = ref(null)

const contributions = [
  {
    title: 'Test Automation',
    subtitle: 'Java, Playwright & Selenium',
    description:
      'Developed and maintained automated test scripts using Java, Playwright and Selenium WebDriver to support reliable software testing and improve test coverage.',
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
      'Applied structured automation practices to create reusable and maintainable test solutions using established test automation frameworks and design patterns.',
    points: [
      'Page Object Model',
      'TestNG and JUnit',
      'Maven-based automation projects',
      'Reusable automation components'
    ]
  },
  {
    title: 'API Testing',
    subtitle: 'REST API & Postman',
    description:
      'Performed API validation using REST APIs and Postman as part of functional and integration testing activities.',
    points: [
      'REST API testing',
      'Postman validation',
      'API integration testing'
    ]
  },
  {
    title: 'Quality Assurance',
    subtitle: 'Functional, Regression & UAT',
    description:
      'Supported multiple testing stages to validate application functionality, business requirements and overall product quality.',
    points: [
      'Functional testing',
      'Regression testing',
      'Smoke and sanity testing',
      'Integration testing',
      'UAT support'
    ]
  },
  {
    title: 'Defect Management',
    subtitle: 'Jira & Root Cause Analysis',
    description:
      'Identified, documented and investigated application issues while supporting defect lifecycle management and root cause analysis.',
    points: [
      'Jira defect management',
      'Issue investigation and reproduction',
      'Root cause analysis',
      'Defect lifecycle management'
    ]
  },
  {
    title: 'Agile & CI Execution',
    subtitle: 'Git, Jenkins & Agile/Scrum',
    description:
      'Worked within Agile/Scrum delivery environments while using source control and CI tools to support software development and testing activities.',
    points: [
      'Git version control',
      'Jenkins',
      'CI execution',
      'Agile/Scrum ceremonies',
      'Cross-functional collaboration'
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

    <!-- =====================================================
         SECTION HEADER
    ====================================================== -->
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


    <!-- =====================================================
         CONTRIBUTION GRID
    ====================================================== -->
    <div class="contribution-grid">

      <article
        v-for="(item, index) in contributions"
        :key="item.title"
        class="contribution-card"
        :class="{ expanded: openIndex === index }"
      >

        <!-- Card Header -->
        <button
          class="card-header"
          type="button"
          :aria-expanded="openIndex === index"
          :aria-controls="`contribution-details-${index}`"
          @click="toggle(index)"
        >

          <!-- Number -->
          <div class="card-number">
            {{ String(index + 1).padStart(2, '0') }}
          </div>


          <!-- Title -->
          <div class="card-title">

            <h3>
              {{ item.title }}
            </h3>

            <span>
              {{ item.subtitle }}
            </span>

          </div>


          <!-- Expand Icon -->
          <div
            class="expand-icon"
            aria-hidden="true"
          >
            {{ openIndex === index ? '−' : '+' }}
          </div>

        </button>


        <!-- Expandable Details -->
        <div
          v-if="openIndex === index"
          :id="`contribution-details-${index}`"
          class="card-details"
        >

          <p>
            {{ item.description }}
          </p>

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

/* =========================================================
   SECTION
========================================================= */

.section {
  width: 100%;
  max-width: 1200px;

  margin: 0 auto;

  padding: 60px 25px;

  background: #ffffff;
}


/* =========================================================
   SECTION HEADER
========================================================= */

.section-header {
  max-width: 700px;

  margin: 0 auto 30px;

  text-align: center;
}


.section-badge {
  display: inline-block;

  padding: 7px 14px;

  margin-bottom: 12px;

  border-radius: 25px;

  background: #e8f8f5;

  border: 1px solid #c9eee8;

  color: #078c80;

  font-size: 11px;

  font-weight: 700;

  letter-spacing: 1px;
}


.section-header h2 {
  margin: 0;

  color: #102a43;

  font-size: clamp(2.3rem, 5vw, 3.3rem);

  line-height: 1.1;

  letter-spacing: -1.5px;
}


.section-header h2 span {
  color: #079f91;
}


.section-header p {
  max-width: 620px;

  margin: 12px auto 0;

  color: #71869a;

  font-size: 0.95rem;

  line-height: 1.6;
}


/* =========================================================
   CONTRIBUTION GRID
========================================================= */

.contribution-grid {
  display: grid;

  grid-template-columns:
    repeat(2, minmax(0, 1fr));

  gap: 12px;
}


/* =========================================================
   CONTRIBUTION CARD
========================================================= */

.contribution-card {
  overflow: hidden;

  border: 1px solid #e1e9ee;

  border-radius: 14px;

  background: #ffffff;

  transition:
    border-color 0.25s ease,
    box-shadow 0.25s ease,
    transform 0.25s ease;
}


.contribution-card:hover {
  transform: translateY(-2px);

  border-color: #a9ddd7;

  box-shadow:
    0 10px 25px rgba(25, 65, 80, 0.07);
}


.contribution-card.expanded {
  border-color: #8fd2ca;

  box-shadow:
    0 10px 25px rgba(25, 65, 80, 0.07);
}


/* =========================================================
   CARD HEADER
========================================================= */

.card-header {
  width: 100%;

  display: grid;

  grid-template-columns:
    42px
    minmax(0, 1fr)
    28px;

  align-items: center;

  gap: 13px;

  padding: 15px 18px;

  border: 0;

  background: transparent;

  text-align: left;

  cursor: pointer;

  font-family: inherit;
}


.card-header:hover {
  background: #fcfefe;
}


.card-header:focus-visible {
  outline: 2px solid #079f91;

  outline-offset: -2px;

  border-radius: 14px;
}


/* =========================================================
   CARD NUMBER
========================================================= */

.card-number {
  width: 40px;

  height: 40px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 10px;

  background: #e8f8f5;

  color: #078c80;

  font-size: 11px;

  font-weight: 800;
}


/* =========================================================
   CARD TITLE
========================================================= */

.card-title {
  min-width: 0;
}


.card-title h3 {
  margin: 0 0 3px;

  color: #102a43;

  font-size: 14px;

  font-weight: 700;

  line-height: 1.3;
}


.card-title span {
  display: block;

  overflow: hidden;

  text-overflow: ellipsis;

  white-space: nowrap;

  color: #71869a;

  font-size: 11px;

  line-height: 1.4;
}


/* =========================================================
   EXPAND ICON
========================================================= */

.expand-icon {
  width: 27px;

  height: 27px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 50%;

  background: #f1faf8;

  color: #078c80;

  font-size: 19px;

  font-weight: 500;

  line-height: 1;

  transition:
    background 0.2s ease,
    transform 0.2s ease;
}


.contribution-card.expanded .expand-icon {
  background: #e1f5f1;
}


/* =========================================================
   CARD DETAILS
========================================================= */

.card-details {
  padding: 0 18px 16px 75px;

  animation: expandContent 0.22s ease;
}


.card-details p {
  margin: 0 0 10px;

  color: #61788d;

  font-size: 12px;

  line-height: 1.65;
}


.card-details ul {
  margin: 0;

  padding-left: 17px;

  color: #516b79;

  font-size: 11px;

  line-height: 1.75;
}


.card-details li {
  padding-left: 2px;
}


.card-details li::marker {
  color: #079f91;
}


/* =========================================================
   ANIMATION
========================================================= */

@keyframes expandContent {

  from {
    opacity: 0;

    transform: translateY(-3px);
  }

  to {
    opacity: 1;

    transform: translateY(0);
  }

}


/* =========================================================
   TABLET
========================================================= */

@media (max-width: 900px) {

  .section {
    padding: 55px 22px;
  }

  .contribution-grid {
    gap: 10px;
  }

}


/* =========================================================
   MOBILE
========================================================= */

@media (max-width: 700px) {

  .section {
    padding: 45px 16px;
  }

  .section-header {
    margin-bottom: 25px;
  }

  .section-header h2 {
    font-size: 2.3rem;
  }

  .section-header p {
    font-size: 0.88rem;

    line-height: 1.55;
  }

  .contribution-grid {
    grid-template-columns: 1fr;

    gap: 10px;
  }

  .card-header {
    grid-template-columns:
      40px
      minmax(0, 1fr)
      27px;

    gap: 11px;

    padding: 13px 14px;
  }

  .card-number {
    width: 38px;

    height: 38px;
  }

  .card-title h3 {
    font-size: 13px;
  }

  .card-title span {
    font-size: 10px;
  }

  .card-details {
    padding: 0 14px 15px;
  }

  .card-details p {
    font-size: 11.5px;
  }

  .card-details ul {
    font-size: 11px;
  }

}


/* =========================================================
   SMALL MOBILE
========================================================= */

@media (max-width: 450px) {

  .section {
    padding: 40px 14px;
  }

  .section-header {
    margin-bottom: 22px;
  }

  .section-header h2 {
    font-size: 2rem;

    letter-spacing: -1px;
  }

  .section-badge {
    font-size: 10px;

    padding: 6px 12px;
  }

  .section-header p {
    margin-top: 10px;

    font-size: 0.82rem;
  }

  .card-header {
    grid-template-columns:
      36px
      minmax(0, 1fr)
      25px;

    gap: 9px;

    padding: 12px;
  }

  .card-number {
    width: 34px;

    height: 34px;

    border-radius: 8px;

    font-size: 9px;
  }

  .card-title h3 {
    font-size: 12px;
  }

  .card-title span {
    font-size: 9.5px;
  }

  .expand-icon {
    width: 24px;

    height: 24px;

    font-size: 17px;
  }

  .card-details {
    padding: 0 12px 14px;
  }

  .card-details p {
    font-size: 11px;

    line-height: 1.6;
  }

  .card-details ul {
    padding-left: 16px;

    font-size: 10.5px;

    line-height: 1.7;
  }

}

</style>