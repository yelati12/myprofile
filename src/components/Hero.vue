<template>
  <section class="hero">
    <div class="hero-container">

      <!-- Left Content -->
      <div class="content">
        <h2 class="name">Sachin Yelati</h2>

        <p class="tag">
          Senior Consultant • Automation Test Engineer
        </p>

        <p class="description">
          Building scalable automation solutions for Banking,
          Financial Services and Healthcare.
        </p>

        <div class="about">
          <h2>About Me</h2>

          <p>
            Results-driven Senior Automation Test Engineer and Senior
            Consultant with 10+ years of experience across Financial Services,
            Retail Banking, Fraud Detection, Insurance, Mortgages and
            Healthcare.
          </p>

          <p>
            Expertise in Playwright, Selenium, Appium, REST API Automation,
            CI/CD, Azure DevOps, Agile Delivery and Team Leadership.
          </p>
        </div>

        <div class="contact-info">
          <div class="contact-card">
            <span>📞</span>
            <span>+44 7440 170994</span>
          </div>

          <div class="contact-card">
            <span>📱</span>
            <span>WhatsApp: +91 9642642411</span>
          </div>

          <div class="contact-card">
            <span>✉️</span>
            <span>yelati.sachin@gmail.com</span>
          </div>

          <div class="contact-card">
            <span>🔗</span>
            <a
              href="https://www.linkedin.com/in/sachin-y-50229364"
              target="_blank"
            >
              LinkedIn Profile
            </a>
          </div>
        </div>

        <div class="buttons">
          <a
            href="https://www.linkedin.com/in/sachin-y-50229364"
            target="_blank"
            class="primary-btn"
          >
            View LinkedIn
          </a>

          <a
            href="mailto:yelati.sachin@gmail.com"
            class="secondary-btn"
          >
            Contact Me
          </a>
        </div>

        <div class="stats">
          <div class="stat-card">
            <h2>10+</h2>
            <p>Years Experience</p>
          </div>

          <div class="stat-card">
            <h2>5+</h2>
            <p>Enterprise Clients</p>
          </div>

          <div class="stat-card">
            <h2>4+</h2>
            <p>Engineers Mentored</p>
          </div>
        </div>
      </div>

      <!-- Right Photo -->
      <div class="photo-section">
        <img
          src="/src/assets/Sachin_Photo.PNG"
          alt="Sachin Yelati"
          class="profile-photo"
        />
      </div>

    </div>
  </section>
</template>

<style scoped>
.hero {
  background: #ffffff;
  padding: 60px 20px;
}

.hero-container {
  max-width: 1400px;
  margin: auto;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 60px;
}

.content {
  flex: 2;
}

.photo-section {
  flex: 1;
  display: flex;
  justify-content: center;
  padding-top: 20px;
}

.profile-photo {
  width: 320px;
  height: 400px;
  object-fit: cover;
  border-radius: 20px;
  border: 5px solid #c0c1c9;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
}

.name {
  font-size: 4rem;
  font-weight: 700;
  color: #111827;
  margin-bottom: 10px;
}

.tag {
  font-size: 1.3rem;
  color: #14b8a6;
  font-weight: 600;
  margin-bottom: 25px;
}

.description {
  max-width: 800px;
  margin-bottom: 30px;
  font-size: 1.1rem;
  line-height: 1.8;
  color: #4b5563;
}

.about {
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  border-radius: 18px;
  padding: 30px;
  margin-bottom: 30px;
}

.about h2 {
  color: #111827;
  margin-bottom: 15px;
}

.about p {
  color: #4b5563;
  line-height: 1.8;
  margin-bottom: 12px;
}

.contact-info {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  margin-bottom: 30px;
}

.contact-card {
  display: flex;
  align-items: center;
  gap: 10px;
  background: white;
  padding: 14px 20px;
  border-radius: 12px;
  border: 1px solid #e5e7eb;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}

.contact-card a {
  color: #14b8a6;
  text-decoration: none;
  font-weight: 600;
}

.contact-card a:hover {
  text-decoration: underline;
}

.buttons {
  margin-bottom: 40px;
}

.primary-btn,
.secondary-btn {
  display: inline-block;
  padding: 14px 28px;
  margin-right: 15px;
  border-radius: 10px;
  text-decoration: none;
  font-weight: 600;
  transition: 0.3s;
}

.primary-btn {
  background: #14b8a6;
  color: #fff;
}

.primary-btn:hover {
  background: #0f9d8a;
}

.secondary-btn {
  border: 2px solid #14b8a6;
  color: #14b8a6;
}

.secondary-btn:hover {
  background: #14b8a6;
  color: white;
}

.stats {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.stat-card {
  min-width: 200px;
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  padding: 25px;
  text-align: center;
}

.stat-card h2 {
  color: #14b8a6;
  font-size: 2.3rem;
  margin-bottom: 8px;
}

.stat-card p {
  color: #4b5563;
}

@media (max-width: 768px) {
  .hero-container {
    flex-direction: column-reverse;
    align-items: center;
  }

  .content {
    text-align: center;
  }

  .name {
    font-size: 2.5rem;
  }

  .profile-photo {
    width: 230px;
    height: 290px;
  }

  .contact-info {
    justify-content: center;
  }

  .buttons a {
    display: block;
    margin: 10px auto;
    width: 220px;
  }

  .stats {
    justify-content: center;
  }
}
</style>