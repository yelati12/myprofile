<script setup>
const education = [
  {
    degree: 'Bachelor of Technology (B.Tech)',
    field: 'Computer Science Engineering',
    institution: 'JNTUH University College of Engineering',
    year: '2021',
    result: '79%'
  },
  {
    degree: 'Intermediate',
    field: 'MPC',
    institution: 'Sri Chaitanya Junior College',
    year: '2017',
    result: '90%'
  },
  {
    degree: 'SSC',
    field: 'Secondary School Certificate',
    institution: 'St. Joseph’s High School',
    year: '2015',
    result: '93%'
  }
]
</script>

<template>
  <section id="education" class="section">

    <!-- Header -->
    <div class="section-header">

      <div class="section-badge">
        ACADEMIC BACKGROUND
      </div>

      <h2>
        Education &
        <span>Qualifications</span>
      </h2>

      <p class="subtitle">
        Academic background in Computer Science and Engineering,
        supported by a strong foundation in software development
        and technology.
      </p>

    </div>


    <!-- Education Cards -->
    <div class="education-grid">

      <div
        v-for="(item, index) in education"
        :key="index"
        class="education-card"
      >

        <!-- Year -->
        <div class="year">
          {{ item.year }}
        </div>


        <!-- Icon -->
        <div class="education-icon">
          🎓
        </div>


        <!-- Content -->
        <div class="education-content">

          <h3>
            {{ item.degree }}
          </h3>

          <h4>
            {{ item.field }}
          </h4>

          <p class="institution">
            {{ item.institution }}
          </p>

          <div class="result">
            <span>Result</span>
            <strong>{{ item.result }}</strong>
          </div>

        </div>

      </div>

    </div>

  </section>
</template>


<style scoped>

/* =========================================
   SECTION
========================================= */

.section {
  max-width: 1200px;

  margin: auto;

  padding: 90px 25px;

  background: #ffffff;
}


/* =========================================
   HEADER
========================================= */

.section-header {
  text-align: center;

  margin-bottom: 55px;
}


.section-badge {
  display: inline-block;

  padding: 8px 16px;

  border-radius: 25px;

  background: #e8f8f5;

  border: 1px solid #c9eee8;

  color: #078c80;

  font-size: 12px;

  font-weight: 700;

  letter-spacing: 1px;

  margin-bottom: 16px;
}


.section-header h2 {
  margin: 0;

  font-size: clamp(2.5rem, 5vw, 3.6rem);

  color: #102a43;

  line-height: 1.1;
}


.section-header h2 span {
  color: #079f91;
}


.subtitle {
  max-width: 700px;

  margin: 18px auto 0;

  color: #71869a;

  font-size: 1rem;

  line-height: 1.7;
}


/* =========================================
   EDUCATION GRID
========================================= */

.education-grid {
  display: grid;

  grid-template-columns:
    repeat(3, minmax(0, 1fr));

  gap: 22px;
}


/* =========================================
   CARD
========================================= */

.education-card {
  position: relative;

  padding: 30px 25px;

  background: #ffffff;

  border: 1px solid #e1e9ee;

  border-radius: 18px;

  box-shadow:
    0 7px 24px rgba(25, 65, 80, 0.06);

  overflow: hidden;

  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease,
    border-color 0.25s ease;
}


.education-card:hover {
  transform: translateY(-5px);

  border-color: #a9ddd7;

  box-shadow:
    0 15px 35px rgba(25, 65, 80, 0.1);
}


/* =========================================
   YEAR
========================================= */

.year {
  position: absolute;

  top: 18px;

  right: 18px;

  padding: 5px 10px;

  border-radius: 15px;

  background: #e8f8f5;

  color: #078c80;

  font-size: 11px;

  font-weight: 700;
}


/* =========================================
   ICON
========================================= */

.education-icon {
  width: 55px;

  height: 55px;

  display: flex;

  align-items: center;

  justify-content: center;

  margin-bottom: 22px;

  border-radius: 15px;

  background: #e8f8f5;

  border: 1px solid #cceee8;

  font-size: 24px;
}


/* =========================================
   CONTENT
========================================= */

.education-content h3 {
  margin: 0 0 7px;

  color: #102a43;

  font-size: 1.15rem;

  font-weight: 750;
}


.education-content h4 {
  margin: 0 0 12px;

  color: #079f91;

  font-size: 0.95rem;

  font-weight: 650;
}


.institution {
  margin: 0;

  color: #61788d;

  font-size: 0.9rem;

  line-height: 1.5;
}


/* =========================================
   RESULT
========================================= */

.result {
  display: flex;

  align-items: center;

  justify-content: space-between;

  margin-top: 20px;

  padding-top: 15px;

  border-top: 1px solid #edf1f3;
}


.result span {
  color: #899bab;

  font-size: 12px;

  font-weight: 600;
}


.result strong {
  color: #078c80;

  font-size: 1.1rem;
}


/* =========================================
   TABLET
========================================= */

@media (max-width: 900px) {

  .education-grid {
    grid-template-columns:
      repeat(2, minmax(0, 1fr));
  }

}


/* =========================================
   MOBILE
========================================= */

@media (max-width: 650px) {

  .section {
    padding: 65px 15px;
  }


  .education-grid {
    grid-template-columns: 1fr;

    gap: 16px;
  }


  .education-card {
    padding: 25px 21px;
  }

}

</style>