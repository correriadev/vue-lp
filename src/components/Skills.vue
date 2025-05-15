<template>
  <section class="skills">
    <div class="container">
      <h2 class="section-title">Main Skills</h2>
      <div class="skills-grid">
        <div class="skill-category">
          <div class="sketch-border"></div>
          <h3>Core Expertise</h3>
          <ul>
            <li>Microservices</li>
            <li>Cloud Computing</li>
            <li>FullStack Development</li>
          </ul>
        </div>
        <div class="skill-category">
          <div class="sketch-border"></div>
          <h3>Technologies</h3>
          <ul>
            <li>.NET C# (Framework to .NET 8)</li>
            <li>Vue.js, Angular, Flutter, React Native</li>
            <li>REST/RESTful APIs, WebSocket</li>
          </ul>
        </div>
        <div class="skill-category">
          <div class="sketch-border"></div>
          <h3>Infrastructure</h3>
          <ul>
            <li>Azure & AWS</li>
            <li>Redis Cache</li>
            <li>ServiceBus & RabbitMQ</li>
          </ul>
        </div>
        <div class="skill-category">
          <div class="sketch-border"></div>
          <h3>Databases</h3>
          <ul>
            <li>SQL Server</li>
            <li>MySQL</li>
            <li>MongoDB & DynamoDB</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Skills'
}
</script>

<style scoped>
.skills {
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

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2.5rem;
  width: 100%;
  max-width: 1200px;
  place-items: center;
  place-content: center;
}

.skill-category {
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

.skill-category:hover {
  transform: translate(-5px, -5px);
}

.skill-category:hover .sketch-border::before {
  transform: translate(8px, 8px);
  transition: transform 0.3s ease;
}

.skill-category h3 {
  color: var(--color-dark);
  font-size: 1.4rem;
  margin-bottom: 1.5rem;
  padding-bottom: 0.8rem;
  border-bottom: 2px solid var(--color-dark);
  position: relative;
}

.skill-category ul {
  list-style: none;
  padding: 0;
}

.skill-category li {
  margin: 1rem 0;
  color: var(--color-dark);
  position: relative;
  padding-left: 1.8rem;
  font-family: var(--font-body);
  font-size: 0.9rem;
}

.skill-category li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: var(--color-dark);
  font-weight: bold;
}

@media (max-width: 1024px) {
  .skills {
    padding: 5rem 0;
  }

  .section-title {
    font-size: 2.5rem;
    margin-bottom: 3.5rem;
  }

  .skills-grid {
    grid-template-columns: repeat(2, minmax(0, 400px));
    max-width: 900px;
  }
}

@media (max-width: 768px) {
  .skills {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2.2rem;
    margin-bottom: 3rem;
  }

  .skills-grid {
    grid-template-columns: minmax(0, 500px);
    max-width: 600px;
  }

  .skill-category {
    padding: 1.5rem;
  }

  .skill-category h3 {
    font-size: 1.3rem;
  }
}

@media (max-width: 480px) {
  .skills {
    padding: 3rem 0;
  }

  .section-title {
    font-size: 1.8rem;
    margin-bottom: 2.5rem;
  }

  .skills-grid {
    grid-template-columns: 1fr;
    max-width: 100%;
    padding: 0 0.5rem;
  }

  .skill-category {
    padding: 1.2rem;
  }

  .skill-category h3 {
    font-size: 1.2rem;
    margin-bottom: 1rem;
  }

  .skill-category li {
    font-size: 0.85rem;
    margin: 0.8rem 0;
  }
}
</style> 