<template>
  <section id="contact" class="contact-section">

    <div class="contact-container">

      <div class="contact-header">

        <div class="section-badge">
          GET IN TOUCH
        </div>

        <h2>
          Let's Connect
        </h2>

        <p>
          Interested in QA, test automation or software quality
          engineering opportunities? Feel free to get in touch.
        </p>

      </div>

      <div class="contact-grid">

        <a
          href="mailto:sumanjali5.v@gmail.com"
          class="contact-card"
        >
          <div class="contact-icon">
            @
          </div>

          <div>
            <span>Email</span>
            <strong>sumanjali5.v@gmail.com</strong>
          </div>
        </a>

        <a
          href="tel:+447585729435"
          class="contact-card"
        >
          <div class="contact-icon">
            ☎
          </div>

          <div>
            <span>Phone</span>
            <strong>+44 7585 729435</strong>
          </div>
        </a>

        <div class="contact-card">
          <div class="contact-icon">
            UK
          </div>

          <div>
            <span>Location</span>
            <strong>Northampton, UK</strong>
          </div>
        </div>

      </div>

    </div>

  </section>
</template>

<style scoped>

.contact-section {
  padding: 90px 25px;

  background: #f7fbfb;
}

.contact-container {
  max-width: 1000px;

  margin: 0 auto;
}

.contact-header {
  max-width: 700px;

  margin: 0 auto 45px;

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

.contact-header h2 {
  margin: 0;

  color: #102a43;

  font-size: clamp(2.4rem, 5vw, 3.5rem);
}

.contact-header p {
  margin: 18px auto 0;

  color: #71869a;

  line-height: 1.7;
}

.contact-grid {
  display: grid;

  grid-template-columns:
    repeat(3, minmax(0, 1fr));

  gap: 16px;
}

.contact-card {
  display: flex;

  align-items: center;

  gap: 14px;

  padding: 20px;

  border: 1px solid #e1e9ee;

  border-radius: 14px;

  background: #ffffff;

  transition: 0.25s ease;
}

.contact-card:hover {
  transform: translateY(-3px);

  border-color: #a9ddd7;

  box-shadow:
    0 10px 25px rgba(25, 65, 80, 0.08);
}

.contact-icon {
  width: 44px;
  height: 44px;

  flex-shrink: 0;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 10px;

  background: #e8f8f5;

  color: #078c80;

  font-size: 13px;

  font-weight: 800;
}

.contact-card div:last-child {
  min-width: 0;

  display: flex;

  flex-direction: column;

  gap: 4px;
}

.contact-card span {
  color: #899bab;

  font-size: 11px;

  font-weight: 700;

  text-transform: uppercase;

  letter-spacing: 0.7px;
}

.contact-card strong {
  color: #304e5c;

  font-size: 12px;

  word-break: break-word;
}

@media (max-width: 750px) {

  .contact-section {
    padding: 65px 16px;
  }

  .contact-grid {
    grid-template-columns: 1fr;
  }

}
</style>