<script setup>
import profilePhoto from '../assets/Sumanjali_photo.PNG'
</script>

<template>
  <section id="home" class="hero">

    <!-- Background decoration -->
    <div class="bg-shape bg-shape-one"></div>
    <div class="bg-shape bg-shape-two"></div>

    <div class="hero-container">

      <!-- =====================================================
           LEFT CONTENT
      ====================================================== -->
      <div class="hero-left">

        <!-- Role Badge -->
        <div class="role-badge">
          <span class="badge-dot"></span>
          Automation Test Engineer | QA
        </div>

        <!-- Name -->
        <h1 class="hero-name">
          Yelati
          <span>Sumanjali</span>
        </h1>

        <!-- Professional Title -->
        <h2 class="hero-title">
          Automation Test Engineer
          <span>• QA</span>
        </h2>

        <!-- Summary -->
        <p class="hero-summary">
          Automation Test Engineer with 2+ years of experience in software
          testing and test automation, with hands-on expertise in Java,
          Playwright, Selenium WebDriver, TestNG, JUnit and Maven.
          Experienced in functional, regression and API testing, defect
          management and root cause analysis across digital and healthcare
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
            <strong>
              Java, Playwright, Selenium WebDriver, TestNG, JUnit and Maven.
            </strong>
          </p>

          <p>
            Experienced in designing and maintaining automation scripts,
            Page Object Model frameworks, functional and regression testing,
            API testing with REST APIs and Postman, and defect management
            using Jira.
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
            <div class="contact-icon">☎</div>

            <div class="contact-text">
              <span>Phone</span>
              <strong>+44 7585 729435</strong>
            </div>
          </div>

          <!-- Email -->
          <div class="contact-card">
            <div class="contact-icon">✉</div>

            <div class="contact-text">
              <span>Email</span>
              <strong>sumanjali5.v@gmail.com</strong>
            </div>
          </div>

          <!-- Location -->
          <div class="contact-card">
            <div class="contact-icon">●</div>

            <div class="contact-text">
              <span>Location</span>
              <strong>Northampton, UK</strong>
            </div>
          </div>

          <!-- Specialisation -->
          <div class="contact-card">
            <div class="contact-icon">▣</div>

            <div class="contact-text">
              <span>Specialisation</span>
              <strong>Test Automation & QA</strong>
            </div>
          </div>

        </div>

        <!-- =================================================
             ACTION BUTTONS
        ================================================== -->
        <div class="hero-actions">

          <!-- Contact -->
          <a
            href="#contact"
            class="primary-button"
          >
            <span>✉</span>
            Contact Me
            <strong>→</strong>
          </a>

          <!-- Experience -->
          <a
            href="#experience"
            class="secondary-button"
          >
            View Experience
            <strong>↓</strong>
          </a>

          <!-- Download Resume -->
          <a
            href="/Sumanjali_Yelati_Resume_Automation_Test_Engineer_Updated.docx"
            download
            class="resume-button"
          >
            <span>↓</span>
            Download Resume
          </a>

        </div>

      </div>


      <!-- =====================================================
           RIGHT CONTENT
      ====================================================== -->
      <div class="hero-right">

        <!-- Profile Photo -->
        <div class="photo-area">

          <div class="photo-decoration"></div>

          <img
            :src="profilePhoto"
            alt="Yelati Sumanjali"
            class="profile-photo"
          />

          <!-- Floating Experience Badge -->
          <div class="experience-badge">
            <strong>2+</strong>

            <span>
              Years<br />
              Experience
            </span>
          </div>

        </div>


        <!-- =================================================
             STATS CARD
        ================================================== -->
        <div class="stats-card">

          <!-- Experience -->
          <div class="stat">
            <strong>2+</strong>

            <span>
              Years<br />
              Experience
            </span>
          </div>

          <div class="stat-divider"></div>

          <!-- QA -->
          <div class="stat">
            <strong>QA</strong>

            <span>
              Test<br />
              Automation
            </span>
          </div>

          <div class="stat-divider"></div>

          <!-- Java -->
          <div class="stat">
            <strong>Java</strong>

            <span>
              Automation
            </span>
          </div>

        </div>

      </div>

    </div>


    <!-- =====================================================
         TECHNOLOGY STRIP
    ====================================================== -->
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

/* =========================================================
   HERO
========================================================= */

.hero {
  position: relative;
  overflow: hidden;

  background:
    radial-gradient(
      circle at 85% 15%,
      rgba(13, 148, 136, 0.10),
      transparent 30%
    ),
    radial-gradient(
      circle at 5% 85%,
      rgba(13, 148, 136, 0.07),
      transparent 28%
    ),
    #ffffff;

  padding: 55px 40px 40px;

  color: #102a43;
}


/* =========================================================
   BACKGROUND SHAPES
========================================================= */

.bg-shape {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
  z-index: 0;
}

.bg-shape-one {
  width: 420px;
  height: 420px;

  top: -230px;
  right: -160px;

  border: 1px solid rgba(13, 148, 136, 0.08);
}

.bg-shape-two {
  width: 300px;
  height: 300px;

  bottom: -180px;
  left: -150px;

  border: 1px solid rgba(13, 148, 136, 0.07);
}


/* =========================================================
   MAIN CONTAINER
========================================================= */

.hero-container {
  position: relative;
  z-index: 1;

  max-width: 1180px;
  margin: 0 auto;

  display: grid;

  grid-template-columns:
    minmax(0, 1.05fr)
    minmax(380px, 0.95fr);

  gap: 50px;

  align-items: center;
}


/* =========================================================
   LEFT SIDE
========================================================= */

.hero-left {
  min-width: 0;
}


/* =========================================================
   ROLE BADGE
========================================================= */

.role-badge {
  display: inline-flex;

  align-items: center;
  gap: 9px;

  padding: 8px 14px;

  border-radius: 999px;

  background: rgba(13, 148, 136, 0.09);
  border: 1px solid rgba(13, 148, 136, 0.16);

  color: #0f766e;

  font-size: 12px;
  font-weight: 700;

  letter-spacing: 0.4px;

  margin-bottom: 18px;
}


.badge-dot {
  width: 8px;
  height: 8px;

  border-radius: 50%;

  background: #0d9488;

  box-shadow:
    0 0 0 4px rgba(13, 148, 136, 0.10);
}


/* =========================================================
   NAME
========================================================= */

.hero-name {
  margin: 0;

  font-size: clamp(3.4rem, 6vw, 5.5rem);

  line-height: 0.94;

  letter-spacing: -3px;

  font-weight: 800;

  color: #102a43;
}


.hero-name span {
  display: block;

  color: #0d9488;
}


/* =========================================================
   TITLE
========================================================= */

.hero-title {
  margin: 18px 0 14px;

  font-size: clamp(1.25rem, 2vw, 1.65rem);

  line-height: 1.3;

  font-weight: 700;

  color: #243b53;
}


.hero-title span {
  color: #0d9488;
}


/* =========================================================
   SUMMARY
========================================================= */

.hero-summary {
  max-width: 690px;

  margin: 0;

  color: #52606d;

  font-size: 15px;

  line-height: 1.75;
}


/* =========================================================
   ABOUT CARD
========================================================= */

.about-card {
  margin-top: 24px;

  padding: 22px 24px;

  background: rgba(255, 255, 255, 0.92);

  border: 1px solid #d9e2ec;

  border-radius: 16px;

  box-shadow:
    0 8px 25px rgba(16, 42, 67, 0.05);
}


.about-heading {
  display: flex;

  align-items: center;

  gap: 10px;

  margin-bottom: 13px;
}


.about-line {
  width: 28px;
  height: 3px;

  border-radius: 999px;

  background: #0d9488;
}


.about-heading h3 {
  margin: 0;

  font-size: 16px;

  color: #102a43;
}


.about-card p {
  margin: 0 0 11px;

  color: #52606d;

  font-size: 13px;

  line-height: 1.7;
}


.about-card p:last-child {
  margin-bottom: 0;
}


.about-card strong {
  color: #243b53;
}


/* =========================================================
   CONTACT GRID
========================================================= */

.contact-grid {
  display: grid;

  grid-template-columns:
    repeat(4, minmax(0, 1fr));

  gap: 10px;

  margin-top: 18px;
}


.contact-card {
  min-width: 0;

  display: flex;

  align-items: center;

  gap: 9px;

  padding: 12px;

  border-radius: 12px;

  background: #ffffff;

  border: 1px solid #e5e7eb;
}


.contact-icon {
  width: 32px;
  height: 32px;

  flex-shrink: 0;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 9px;

  background: rgba(13, 148, 136, 0.10);

  color: #0d9488;

  font-size: 14px;
}


.contact-text {
  min-width: 0;

  display: flex;

  flex-direction: column;

  gap: 2px;
}


.contact-text span {
  font-size: 9px;

  text-transform: uppercase;

  letter-spacing: 0.7px;

  color: #829ab1;
}


.contact-text strong {
  overflow: hidden;

  text-overflow: ellipsis;

  white-space: nowrap;

  font-size: 11px;

  color: #243b53;
}


/* =========================================================
   ACTION BUTTONS
========================================================= */

.hero-actions {
  display: flex;

  align-items: stretch;

  gap: 10px;

  margin-top: 20px;
}


.primary-button,
.secondary-button,
.resume-button {
  min-height: 48px;

  display: inline-flex;

  align-items: center;
  justify-content: center;

  gap: 9px;

  padding: 0 18px;

  border-radius: 12px;

  font-size: 12px;

  font-weight: 700;

  text-decoration: none;

  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease,
    background 0.2s ease,
    border-color 0.2s ease;
}


/* =========================================================
   PRIMARY BUTTON
========================================================= */

.primary-button {
  background: #0d9488;

  color: #ffffff;

  box-shadow:
    0 7px 18px rgba(13, 148, 136, 0.20);
}


.primary-button:hover {
  transform: translateY(-2px);

  background: #0f766e;

  box-shadow:
    0 10px 24px rgba(13, 148, 136, 0.25);
}


.primary-button span {
  font-size: 14px;
}


/* =========================================================
   SECONDARY BUTTON
========================================================= */

.secondary-button {
  background: #ffffff;

  color: #243b53;

  border: 1px solid #d9e2ec;
}


.secondary-button:hover {
  transform: translateY(-2px);

  border-color: #0d9488;

  color: #0d9488;

  box-shadow:
    0 8px 20px rgba(16, 42, 67, 0.08);
}


.secondary-button strong {
  color: #0d9488;

  font-size: 15px;
}


/* =========================================================
   RESUME BUTTON
========================================================= */

.resume-button {
  background: #102a43;

  color: #ffffff;

  border: 1px solid #102a43;

  box-shadow:
    0 7px 17px rgba(16, 42, 67, 0.15);
}


.resume-button:hover {
  transform: translateY(-2px);

  background: #183b56;

  border-color: #183b56;

  box-shadow:
    0 10px 22px rgba(16, 42, 67, 0.20);
}


.resume-button span {
  font-size: 16px;
}


.resume-button::after {
  content: "DOCX";

  font-size: 8px;

  padding: 3px 5px;

  border-radius: 4px;

  background: rgba(255, 255, 255, 0.15);

  letter-spacing: 0.3px;
}


/* =========================================================
   RIGHT SIDE
========================================================= */

.hero-right {
  min-width: 0;

  display: flex;

  flex-direction: column;

  align-items: center;
}


/* =========================================================
   PHOTO AREA
========================================================= */

.photo-area {
  position: relative;

  width: min(100%, 500px);

  height: 500px;

  display: flex;

  align-items: center;
  justify-content: center;
}


.photo-decoration {
  position: absolute;

  width: 420px;
  height: 420px;

  border-radius: 50%;

  background:
    radial-gradient(
      circle,
      rgba(13, 148, 136, 0.12),
      rgba(13, 148, 136, 0.04) 58%,
      transparent 59%
    );

  border: 1px solid rgba(13, 148, 136, 0.12);
}


.profile-photo {
  position: relative;

  z-index: 2;

  width: 360px;
  height: 430px;

  object-fit: cover;

  object-position: center top;

  border-radius: 22px;

  background: #ffffff;

  border: 7px solid #ffffff;

  box-shadow:
    0 22px 55px rgba(16, 42, 67, 0.16);
}


/* =========================================================
   EXPERIENCE BADGE
========================================================= */

.experience-badge {
  position: absolute;

  z-index: 3;

  right: 22px;
  bottom: 30px;

  display: flex;

  align-items: center;

  gap: 10px;

  padding: 12px 16px;

  border-radius: 14px;

  background: #ffffff;

  border: 1px solid #d9e2ec;

  box-shadow:
    0 12px 30px rgba(16, 42, 67, 0.13);
}


.experience-badge strong {
  font-size: 25px;

  line-height: 1;

  color: #0d9488;
}


.experience-badge span {
  font-size: 10px;

  line-height: 1.35;

  color: #52606d;

  font-weight: 600;
}


/* =========================================================
   STATS CARD
========================================================= */

.stats-card {
  width: min(100%, 500px);

  display: flex;

  align-items: center;
  justify-content: space-around;

  padding: 16px 20px;

  background: #ffffff;

  border: 1px solid #d9e2ec;

  border-radius: 16px;

  box-shadow:
    0 10px 30px rgba(16, 42, 67, 0.07);
}


.stat {
  flex: 1;

  text-align: center;

  display: flex;

  flex-direction: column;

  gap: 4px;
}


.stat strong {
  font-size: 18px;

  color: #0d9488;
}


.stat span {
  font-size: 9px;

  line-height: 1.3;

  text-transform: uppercase;

  letter-spacing: 0.6px;

  color: #829ab1;
}


.stat-divider {
  width: 1px;

  height: 34px;

  background: #e5e7eb;
}


/* =========================================================
   TECHNOLOGY STRIP
========================================================= */

.technology-strip {
  position: relative;

  z-index: 1;

  max-width: 1180px;

  margin: 40px auto 0;

  padding-top: 18px;

  border-top: 1px solid #e5e7eb;

  display: flex;

  align-items: center;
  justify-content: center;

  flex-wrap: wrap;

  gap: 10px;
}


.technology-strip span {
  padding: 7px 11px;

  border-radius: 999px;

  background: #f8fafc;

  border: 1px solid #e5e7eb;

  color: #52606d;

  font-size: 10px;

  font-weight: 600;
}


/* =========================================================
   TABLET
========================================================= */

@media (max-width: 1050px) {

  .hero {
    padding: 45px 28px 35px;
  }

  .hero-container {
    grid-template-columns: 1fr;

    gap: 40px;
  }

  .hero-left {
    max-width: 850px;

    margin: 0 auto;
  }

  .hero-right {
    max-width: 600px;

    width: 100%;

    margin: 0 auto;
  }

  .hero-name {
    font-size: clamp(3.5rem, 8vw, 5rem);
  }

  .photo-area {
    width: 390px;

    height: 420px;
  }

  .profile-photo {
    width: 320px;

    height: 390px;
  }

  .photo-decoration {
    width: 370px;

    height: 370px;
  }

  .contact-grid {
    grid-template-columns: repeat(2, 1fr);
  }

}


/* =========================================================
   MOBILE / TABLET
========================================================= */

@media (max-width: 750px) {

  .hero {
    padding: 38px 20px 30px;
  }

  .hero-container {
    gap: 30px;
  }

  .hero-name {
    font-size: 3.8rem;

    letter-spacing: -2px;
  }

  .hero-title {
    font-size: 1.2rem;
  }

  .hero-summary {
    font-size: 14px;
  }

  .about-card {
    padding: 19px;
  }

  .contact-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .photo-area {
    width: 390px;

    max-width: 100%;

    height: 420px;
  }

  .profile-photo {
    width: 310px;

    height: 380px;
  }

  .photo-decoration {
    width: 360px;

    height: 360px;
  }

}


/* =========================================================
   SMALL MOBILE
========================================================= */

@media (max-width: 550px) {

  .hero {
    padding: 32px 16px 25px;
  }

  .hero-container {
    gap: 25px;
  }

  .role-badge {
    font-size: 10px;

    padding: 7px 11px;
  }

  .hero-name {
    font-size: 3.05rem;

    line-height: 0.98;

    letter-spacing: -1.5px;
  }

  .hero-title {
    margin-top: 14px;

    font-size: 1.08rem;
  }

  .hero-summary {
    font-size: 13px;

    line-height: 1.65;
  }


  /* About */
  .about-card {
    margin-top: 18px;

    padding: 17px;
  }

  .about-card p {
    font-size: 12px;

    line-height: 1.65;
  }


  /* Contact */
  .contact-grid {
    grid-template-columns: 1fr;

    gap: 8px;
  }


  /* Buttons */
  .hero-actions {
    display: grid;

    grid-template-columns: repeat(3, 1fr);

    gap: 8px;

    margin-top: 18px;
  }

  .primary-button,
  .secondary-button,
  .resume-button {
    width: 100%;

    min-height: 44px;

    padding: 0 8px;

    gap: 5px;

    font-size: 10.5px;

    border-radius: 10px;
  }

  .primary-button strong,
  .secondary-button strong,
  .resume-button span {
    font-size: 14px;
  }

  .resume-button::after {
    font-size: 6.5px;

    padding: 2px 4px;
  }


  /* Photo */
  .photo-area {
    width: 330px;

    max-width: 100%;

    height: 350px;
  }

  .profile-photo {
    width: 270px;

    height: 320px;

    border-width: 5px;

    border-radius: 18px;
  }

  .photo-decoration {
    width: 300px;

    height: 300px;
  }

  .experience-badge {
    right: 4px;

    bottom: 18px;

    padding: 9px 12px;
  }

  .experience-badge strong {
    font-size: 20px;
  }

  .experience-badge span {
    font-size: 8px;
  }


  /* Stats */
  .stats-card {
    padding: 13px 10px;

    border-radius: 13px;
  }

  .stat strong {
    font-size: 15px;
  }

  .stat span {
    font-size: 7px;
  }

  .stat-divider {
    height: 28px;
  }


  /* Technology */
  .technology-strip {
    margin-top: 28px;

    padding-top: 14px;

    gap: 6px;
  }

  .technology-strip span {
    font-size: 8px;

    padding: 6px 8px;
  }

}


/* =========================================================
   VERY SMALL MOBILE
========================================================= */

@media (max-width: 380px) {

  .hero {
    padding-left: 13px;

    padding-right: 13px;
  }

  .hero-name {
    font-size: 2.75rem;
  }

  .hero-title {
    font-size: 1rem;
  }

  .hero-summary {
    font-size: 12px;
  }

  .hero-actions {
    grid-template-columns: 1fr;
  }

  .primary-button,
  .secondary-button,
  .resume-button {
    min-height: 44px;

    font-size: 11px;
  }

  .photo-area {
    height: 330px;
  }

  .profile-photo {
    width: 245px;

    height: 300px;
  }

  .photo-decoration {
    width: 280px;

    height: 280px;
  }

}

</style>