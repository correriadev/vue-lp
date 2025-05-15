<template>
  <section class="experience">
    <div class="container">
      <h2 class="section-title">Professional Experience</h2>
      <div class="experience-blocks">
        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>Paraná Banco S/A</h3>
          <div class="role">Technical Leader</div>
          <div class="period">November 2024 - Present</div>
          <ul>
            <li>Technical decisions for mobile app development (Android/iOS) using React Native</li>
          </ul>
        </div>

        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>Paraná Banco S/A</h3>
          <div class="role">Senior .NET Developer</div>
          <div class="period">February 2022 - November 2024</div>
          <ul>
            <li>Development with .NET, Azure, messaging systems, and TDD</li>
            <li>Technical support in CI/CD publication cycles</li>
          </ul>
        </div>

        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>Toro Investimentos</h3>
          <div class="role">Senior .NET Developer</div>
          <div class="period">May 2021 - February 2022</div>
          <ul>
            <li>Investment/trading sector development with .NET, SQL Server, AWS</li>
          </ul>
        </div>

        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>Paraná Banco S/A</h3>
          <div class="role">Full Stack Developer</div>
          <div class="period">November 2019 - May 2021</div>
          <ul>
            <li>Financial sector solutions using .NET, React, Azure and microservices</li>
          </ul>
        </div>

        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>DB1 Global Software</h3>
          <div class="role">Full Stack Developer</div>
          <div class="period">November 2018 - November 2019</div>
          <ul>
            <li>Large-scale project for the educational sector using .NET and Angular with microservices and monolithic architectures</li>
          </ul>
        </div>

        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>UDS Tecnologia</h3>
          <div class="role">Full Stack Developer</div>
          <div class="period">October 2017 - November 2018</div>
          <ul>
            <li>Development of e-commerce and backoffice projects using Vue.js, .NET and React Native for financial and retail sectors</li>
          </ul>
        </div>

        <div class="experience-block">
          <div class="sketch-border"></div>
          <h3>TecnoSpeed TI</h3>
          <div class="role">Technical Consultant</div>
          <div class="period">November 2015 - October 2017</div>
          <ul>
            <li>Direct support to development teams as a consultant, providing technical support for a complete tax document integration and printing module (Sefaz, DANFe, NFe, NFCe, NFSe, CTe, Direct Bank Slip)</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Experience'
}
</script>

<style scoped>
.experience {
  padding: 6rem 0;
  background-color: var(--color-light);
  position: relative;
  width: 100%;
  display: flex;
  justify-content: center;
}

.container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.section-title {
  text-align: center;
  font-size: 2.8rem;
  margin-bottom: 4rem;
  color: var(--color-dark);
  position: relative;
  width: fit-content;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: -20px;
  right: -20px;
  height: 2px;
  background: var(--color-dark);
  transform: skew(-15deg);
}

.experience-blocks {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2.5rem;
  width: 100%;
  max-width: 1200px;
  padding: 0 20px;
}

.experience-block {
  background: var(--color-light);
  padding: 2rem;
  position: relative;
  transition: transform 0.3s ease;
}

.sketch-border {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border: 2px solid var(--color-dark);
  pointer-events: none;
}

.sketch-border::before {
  content: '';
  position: absolute;
  top: 5px;
  left: 5px;
  right: -5px;
  bottom: -5px;
  border: 2px solid var(--color-dark);
  opacity: 0.3;
}

.experience-block:hover {
  transform: translate(-5px, -5px);
}

.experience-block:hover .sketch-border::before {
  transform: translate(8px, 8px);
  transition: transform 0.3s ease;
}

h3 {
  color: var(--color-dark);
  font-size: 1.4rem;
  margin-bottom: 0.5rem;
}

.role {
  color: var(--color-accent);
  font-weight: 600;
  margin-bottom: 0.25rem;
  font-family: var(--font-body);
  font-size: 1rem;
}

.period {
  color: var(--color-accent);
  font-size: 0.9rem;
  margin-bottom: 1rem;
  font-family: var(--font-body);
  font-style: italic;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 0.8rem 0;
  color: var(--color-dark);
  position: relative;
  padding-left: 1.8rem;
  font-family: var(--font-body);
  font-size: 0.9rem;
}

li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: var(--color-dark);
  font-weight: bold;
}

@media (max-width: 1024px) {
  .experience {
    padding: 5rem 0;
  }

  .section-title {
    font-size: 2.5rem;
    margin-bottom: 3.5rem;
  }

  .experience-blocks {
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    max-width: 900px;
  }
}

@media (max-width: 768px) {
  .experience {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2.2rem;
    margin-bottom: 3rem;
  }

  .experience-blocks {
    grid-template-columns: 1fr;
    max-width: 600px;
  }

  .experience-block {
    padding: 1.5rem;
  }
}

@media (max-width: 480px) {
  .experience {
    padding: 3rem 0;
  }

  .section-title {
    font-size: 1.8rem;
    margin-bottom: 2.5rem;
  }

  .experience-blocks {
    padding: 0 15px;
  }

  .experience-block {
    padding: 1.2rem;
  }

  li {
    font-size: 0.85rem;
    margin: 0.8rem 0;
  }
}
</style> 