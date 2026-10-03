<script setup>
import profilePhoto from '../assets/Sumanjali_photo.PNG'
</script>

<template>
  <section id="home" class="hero">

    <!-- Decorative background -->
    <div class="bg-shape bg-shape-one"></div>
    <div class="bg-shape bg-shape-two"></div>

    <div class="hero-container">

      <!-- =================================================
           LEFT CONTENT
      ================================================== -->
      <div class="hero-left">

        <!-- Badge -->
        <div class="role-badge">
          <span class="badge-dot"></span>
          Automation Test Engineer | QA
        </div>

        <!-- Name -->
        <h1 class="hero-name">
          Yelati
          <span>Sumanjali</span>
        </h1>

        <!-- Title -->
        <h2 class="hero-title">
          Automation Test Engineer
          <span>• QA</span>
        </h2>

        <!-- Summary -->
        <p class="hero-summary">
          Computer Science graduate with 2+ years of experience
          in technical support, incident triage, root cause analysis
          and software test automation across digital and healthcare
          environments.
        </p>


        <!-- =================================================
             ABOUT ME
        ================================================== -->

        <div class="about-card">

          <div class="about-heading">
            <span class="about-line"></span>

            <h3>About Me</h3>
          </div>

          <p>
            Computer Science graduate with a B.Tech in Computer Science
            Engineering and 79% marks, building a career in software test
            automation with hands-on experience in
            <strong>Java, Playwright, Selenium WebDriver, TestNG,
            JUnit and Maven.</strong>
          </p>

          <p>
            Experienced in designing and maintaining automation scripts,
            Page Object Model frameworks, functional and regression
            testing, API testing with REST APIs and Postman, and defect
            management using Jira.
          </p>

          <p>
            Strong background in defect investigation, root cause analysis,
            Agile/Scrum collaboration and working with developers,
            Business Analysts and QA teams throughout the SDLC and STLC.
          </p>

        </div>


        <!-- =================================================
             CONTACT INFORMATION
        ================================================== -->

        <div class="contact-grid">

          <!-- Phone -->
          <div class="contact-card">

            <div class="contact-icon">
              ☎
            </div>

            <div>
              <span>Phone</span>
              <strong>+44 7585 729435</strong>
            </div>

          </div>


          <!-- Email -->
          <div class="contact-card">

            <div class="contact-icon">
              ✉
            </div>

            <div>
              <span>Email</span>
              <strong>sumanjali5.v@gmail.com</strong>
            </div>

          </div>


          <!-- Location -->
          <div class="contact-card">

            <div class="contact-icon">
              ●
            </div>

            <div>
              <span>Location</span>
              <strong>Northampton, UK</strong>
            </div>

          </div>


          <!-- Specialisation -->
          <div class="contact-card">

            <div class="contact-icon">
              ▣
            </div>

            <div>
              <span>Specialisation</span>
              <strong>Test Automation & QA</strong>
            </div>

          </div>

        </div>


        <!-- =================================================
             ACTION BUTTONS
        ================================================== -->

        <div class="hero-actions">

          <a
            href="#contact"
            class="primary-button"
          >
            <span>✉</span>
            Contact Me
            <strong>→</strong>
          </a>


          <a
            href="#experience"
            class="secondary-button"
          >
            View Experience
            <strong>↓</strong>
          </a>

        </div>

      </div>


      <!-- =================================================
           RIGHT CONTENT
      ================================================== -->

      <div class="hero-right">

        <!-- Photo -->
        <div class="photo-area">

          <div class="photo-decoration"></div>

          <img
            :src="profilePhoto"
            alt="Yelati Sumanjali"
            class="profile-photo"
          />

          <!-- Experience badge -->
          <div class="experience-badge">

            <strong>2+</strong>

            <span>
              Years<br />
              Experience
            </span>

          </div>

        </div>


        <!-- =================================================
             QUICK STATS
        ================================================== -->

        <div class="stats-card">

          <div class="stat">

            <strong>2+</strong>

            <span>
              Years<br />
              Experience
            </span>

          </div>


          <div class="stat-divider"></div>


          <div class="stat">

            <strong>QA</strong>

            <span>
              Test<br />
              Automation
            </span>

          </div>


          <div class="stat-divider"></div>


          <div class="stat">

            <strong>Java</strong>

            <span>
              Automation
            </span>

          </div>

        </div>

      </div>

    </div>


    <!-- =================================================
         TECHNOLOGY STRIP
    ================================================== -->

    <div class="technology-strip">

      <span>Java</span>
      <span>Playwright</span>
      <span>Selenium</span>
      <span>TestNG</span>
      <span>JUnit</span>
      <span>Maven</span>
      <span>REST API</span>
      <span>Jira</span>
      <span>Git</span>
      <span>CI/CD</span>
      <span>Agile/Scrum</span>

    </div>

  </section>
</template>


<style scoped>

/* =====================================================
   HERO
===================================================== */

.hero {
  position: relative;

  width: 100%;
  min-height: 100vh;

  padding: 55px 5% 35px;

  background:
    radial-gradient(
      circle at 85% 15%,
      rgba(15, 174, 157, 0.10),
      transparent 25%
    ),
    #ffffff;

  overflow: hidden;
}


/* =====================================================
   BACKGROUND SHAPES
===================================================== */

.bg-shape {
  position: absolute;

  border-radius: 50%;

  pointer-events: none;

  background: rgba(225, 247, 244, 0.65);
}

.bg-shape-one {
  width: 180px;
  height: 180px;

  right: -70px;
  top: -60px;
}

.bg-shape-two {
  width: 220px;
  height: 220px;

  left: -120px;
  bottom: -130px;
}


/* =====================================================
   MAIN CONTAINER
===================================================== */

.hero-container {
  position: relative;

  z-index: 2;

  width: 100%;
  max-width: 1250px;

  margin: 0 auto;

  display: grid;

  grid-template-columns:
    minmax(0, 1.08fr)
    minmax(420px, 0.92fr);

  gap: 55px;

  align-items: start;
}


/* =====================================================
   LEFT
===================================================== */

.hero-left {
  width: 100%;
}


/* =====================================================
   BADGE
===================================================== */

.role-badge {
  display: inline-flex;

  align-items: center;

  gap: 10px;

  padding: 10px 17px;

  border-radius: 30px;

  background: #e7f8f5;

  border: 1px solid #c9eee8;

  color: #087f76;

  font-size: 14px;

  font-weight: 700;
}

.badge-dot {
  width: 10px;
  height: 10px;

  border-radius: 50%;

  background: #079f91;
}


/* =====================================================
   NAME
===================================================== */

.hero-name {
  margin: 22px 0 12px;

  color: #102a43;

  font-size: clamp(
    4rem,
    6vw,
    6.3rem
  );

  line-height: 0.94;

  letter-spacing: -4px;

  font-weight: 800;
}

.hero-name span {
  display: block;

  color: #079f91;
}


/* =====================================================
   TITLE
===================================================== */

.hero-title {
  margin: 25px 0 15px;

  color: #183b56;

  font-size: clamp(
    1.4rem,
    2vw,
    2rem
  );

  font-weight: 750;
}

.hero-title span {
  color: #102a43;
}


/* =====================================================
   SUMMARY
===================================================== */

.hero-summary {
  max-width: 690px;

  margin: 0;

  color: #61788d;

  font-size: 17px;

  line-height: 1.55;
}


/* =====================================================
   ABOUT CARD
===================================================== */

.about-card {
  margin-top: 22px;

  padding: 22px 28px;

  background:
    linear-gradient(
      135deg,
      #f0faf8,
      #f8fcfc
    );

  border: 1px solid #dcefeb;

  border-radius: 17px;

  box-shadow:
    0 8px 25px
    rgba(24, 75, 80, 0.04);
}

.about-heading {
  display: flex;

  align-items: center;

  gap: 12px;

  margin-bottom: 12px;
}

.about-line {
  width: 5px;
  height: 32px;

  border-radius: 10px;

  background: #079f91;
}

.about-heading h3 {
  margin: 0;

  color: #183b56;

  font-size: 22px;
}

.about-card p {
  margin: 0 0 10px;

  color: #4e6578;

  font-size: 14px;

  line-height: 1.55;
}

.about-card p:last-child {
  margin-bottom: 0;
}

.about-card strong {
  color: #183b56;
}


/* =====================================================
   CONTACT GRID
===================================================== */

.contact-grid {
  display: grid;

  grid-template-columns:
    repeat(4, minmax(0, 1fr));

  gap: 12px;

  margin-top: 22px;
}

.contact-card {
  min-height: 78px;

  display: flex;

  align-items: center;

  gap: 10px;

  padding: 12px;

  background: #ffffff;

  border: 1px solid #e0e8ed;

  border-radius: 12px;

  box-shadow:
    0 5px 15px
    rgba(25, 65, 80, 0.04);
}

.contact-icon {
  width: 42px;
  height: 42px;

  flex-shrink: 0;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 50%;

  background: #e1f7f3;

  color: #078c80;

  font-size: 20px;
}

.contact-card div:last-child {
  min-width: 0;
}

.contact-card span {
  display: block;

  margin-bottom: 4px;

  color: #8296a5;

  font-size: 12px;
}

.contact-card strong {
  display: block;

  color: #304f61;

  font-size: 11px;

  white-space: nowrap;
}


/* =====================================================
   BUTTONS
===================================================== */

.hero-actions {
  display: flex;

  gap: 14px;

  margin-top: 30px;
}

.primary-button,
.secondary-button {
  min-height: 53px;

  display: inline-flex;

  align-items: center;

  justify-content: center;

  gap: 12px;

  padding: 0 25px;

  border-radius: 14px;

  font-size: 14px;

  font-weight: 700;

  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.primary-button {
  background: #079f91;

  color: #ffffff;

  box-shadow:
    0 10px 22px
    rgba(7, 159, 145, 0.18);
}

.primary-button:hover {
  transform: translateY(-2px);

  box-shadow:
    0 14px 28px
    rgba(7, 159, 145, 0.25);
}

.primary-button strong {
  font-size: 18px;
}

.secondary-button {
  min-width: 225px;

  background: #ffffff;

  border: 2px solid #079f91;

  color: #078c80;
}

.secondary-button:hover {
  transform: translateY(-2px);

  background: #f2fbfa;
}

.secondary-button strong {
  font-size: 20px;
}


/* =====================================================
   RIGHT SIDE
===================================================== */

.hero-right {
  position: relative;

  min-height: 690px;

  display: flex;

  flex-direction: column;

  align-items: center;
}


/* =====================================================
   PHOTO
===================================================== */

.photo-area {
  position: relative;

  width: min(
    100%,
    560px
  );

  height: 570px;

  margin-top: -10px;
}

.photo-decoration {
  position: absolute;

  inset: 70px 35px 40px 40px;

  border-radius: 45% 12% 35% 12%;

  background: #dff5f1;

  transform: rotate(7deg);
}

.photo-decoration::after {
  content: "";

  position: absolute;

  inset: 35px 0 0 0;

  border: 2px solid #079f91;

  border-radius: 30% 15% 30% 10%;

  transform: rotate(-4deg);
}

.profile-photo {
  position: relative;

  z-index: 2;

  width: 100%;
  height: 100%;

  object-fit: cover;

  /*
   * Keep the face and shoulders visible.
   * The original photo is portrait-oriented,
   * so don't position it too high.
   */
  object-position: center 18%;

  border-radius: 42% 16% 38% 14%;

  filter: saturate(0.98);

  box-shadow:
    0 25px 50px
    rgba(35, 70, 80, 0.10);
}

/* =====================================================
   EXPERIENCE BADGE
===================================================== */

.experience-badge {
  position: absolute;

  z-index: 5;

  right: 0;

  bottom: 55px;

  width: 145px;
  height: 145px;

  display: flex;

  flex-direction: column;

  justify-content: center;

  align-items: center;

  border-radius: 28px;

  background:
    linear-gradient(
      145deg,
      #078c80,
      #075f5b
    );

  color: #ffffff;

  box-shadow:
    0 18px 35px
    rgba(7, 100, 93, 0.22);
}

.experience-badge strong {
  font-size: 39px;

  line-height: 1;
}

.experience-badge span {
  margin-top: 8px;

  text-align: center;

  font-size: 13px;

  line-height: 1.4;
}


/* =====================================================
   STATS
===================================================== */

.stats-card {
  width: min(
    100%,
    560px
  );

  min-height: 100px;

  display: flex;

  align-items: center;

  justify-content: space-around;

  margin-top: 5px;

  padding: 15px;

  background:
    linear-gradient(
      135deg,
      #f0faf8,
      #f7fcfc
    );

  border-radius: 20px;
}

.stat {
  flex: 1;

  text-align: center;
}

.stat strong {
  display: block;

  color: #079f91;

  font-size: 25px;

  line-height: 1.2;
}

.stat span {
  display: block;

  margin-top: 5px;

  color: #71869a;

  font-size: 11px;

  line-height: 1.35;
}

.stat-divider {
  width: 1px;

  height: 55px;

  background: #c8ddda;
}


/* =====================================================
   TECHNOLOGY STRIP
===================================================== */

.technology-strip {
  position: relative;

  z-index: 3;

  width: 100%;

  max-width: 1120px;

  margin: 25px auto 0;

  display: flex;

  align-items: center;

  justify-content: center;

  flex-wrap: wrap;

  gap: 12px;
}

.technology-strip span {
  padding: 11px 18px;

  border-radius: 30px;

  background: #e5f8f4;

  color: #078c80;

  font-size: 12px;

  font-weight: 700;
}


/* =====================================================
   LARGE TABLET
===================================================== */

@media (max-width: 1100px) {

  .hero {
    padding-left: 30px;
    padding-right: 30px;
  }

  .hero-container {
    grid-template-columns: 1fr;

    max-width: 850px;
  }

  .hero-left {
    text-align: center;
  }

  .hero-summary {
    margin-left: auto;
    margin-right: auto;
  }

  .about-card {
    text-align: left;
  }

  .hero-actions {
    justify-content: center;
  }

  .hero-right {
    min-height: auto;
  }

  .photo-area {
    width: 450px;
    height: 500px;
  }

  .stats-card {
    margin-bottom: 20px;
  }

}


/* =====================================================
   TABLET
===================================================== */

@media (max-width: 750px) {

  .hero {
    padding: 45px 20px 30px;
  }

  .hero-name {
    font-size: 4.4rem;

    letter-spacing: -3px;
  }

  .contact-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .photo-area {
    width: 400px;
    height: 450px;
  }

}


/* =====================================================
   MOBILE
===================================================== */

@media (max-width: 550px) {

  .hero {
    padding: 35px 15px 25px;
  }

  .role-badge {
    font-size: 11px;

    padding: 8px 13px;
  }

  .hero-name {
    margin-top: 18px;

    font-size: 3.4rem;

    letter-spacing: -2px;
  }

  .hero-title {
    font-size: 1.25rem;

    margin-top: 18px;
  }

  .hero-summary {
    font-size: 14px;
  }

  .about-card {
    padding: 18px;

    border-radius: 14px;
  }

  .about-card p {
    font-size: 13px;
  }

  .contact-grid {
    grid-template-columns: 1fr;
  }

  .contact-card {
    min-height: 65px;
  }

  .hero-actions {
    flex-direction: column;
  }

  .primary-button,
  .secondary-button {
    width: 100%;
  }

  .hero-right {
    width: 100%;
  }

  .photo-area {
    width: 320px;
    height: 370px;
  }

  .experience-badge {
    width: 110px;
    height: 110px;

    right: -5px;

    bottom: 30px;
  }

  .experience-badge strong {
    font-size: 30px;
  }

  .experience-badge span {
    font-size: 10px;
  }

  .stats-card {
    min-height: 85px;

    border-radius: 15px;
  }

  .stat strong {
    font-size: 19px;
  }

  .stat span {
    font-size: 9px;
  }

  .technology-strip {
    gap: 7px;
  }

  .technology-strip span {
    padding: 8px 12px;

    font-size: 10px;
  }

}


/* =====================================================
   SMALL MOBILE
===================================================== */

@media (max-width: 380px) {

  .hero-name {
    font-size: 2.9rem;
  }

  .photo-area {
    width: 285px;
    height: 335px;
  }

  .experience-badge {
    width: 95px;
    height: 95px;
  }

  .experience-badge strong {
    font-size: 25px;
  }

}
</style>