<template>
  <header class="header">
    <div class="sketch-bg"></div>
    <div class="container">
      <div class="header-content">
        <div class="profile-image">
          <div class="sketch-frame"></div>
        </div>
        <div class="text-content">
          <h1>Artur de Souza Corrêa</h1>
          <h2>Software Engineer</h2>
          <div class="location">
            <i class="fas fa-map-marker-alt"></i>
            Curitiba, Paraná, Brasil
          </div>
          <div class="social-links">
            <a href="https://www.linkedin.com/in/artur-de-souza-corrêa-b42028158" target="_blank" class="social-link">
              <i class="fab fa-linkedin"></i>
            </a>
            <a href="https://github.com/correriadev" target="_blank" class="social-link">
              <i class="fab fa-github"></i>
            </a>
            <a href="mailto:correa.dev@gmail.com" class="social-link">
              <i class="fas fa-envelope"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header {
  position: relative;
  color: var(--color-dark);
  padding: 6rem 0;
  overflow: hidden;
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

.sketch-bg {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--color-light);
  opacity: 0.8;
  z-index: 1;
}

.sketch-bg::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='sketch'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.04' numOctaves='5'/%3E%3CfeDisplacementMap in='SourceGraphic' scale='10'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23sketch)' fill='none' stroke='white' stroke-width='0.5'/%3E%3C/svg%3E");
  opacity: 0.15;
}

.header-content {
  position: relative;
  z-index: 2;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 4rem;
  width: 100%;
  max-width: 1200px;
}

.profile-image {
  width: 300px;
  height: 300px;
  position: relative;
  border: 2px solid var(--color-dark);
  background: url('/profile_blame.png') center/cover;
  filter: grayscale(100%) contrast(120%);
}

.sketch-frame {
  position: absolute;
  top: -10px;
  left: -10px;
  right: -10px;
  bottom: -10px;
  border: 2px solid var(--color-dark);
  pointer-events: none;
}

.sketch-frame::before {
  content: '';
  position: absolute;
  top: 10px;
  left: 10px;
  right: -10px;
  bottom: -10px;
  border: 2px solid var(--color-dark);
  opacity: 0.3;
}

.text-content {
  flex: 1;
  max-width: 600px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

h1 {
  font-size: 3.5rem;
  margin-bottom: 0.5rem;
  font-weight: 700;
  position: relative;
  display: inline-block;
}

h1::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 2px;
  background: var(--color-dark);
  transform: skew(-15deg);
}

h2 {
  font-size: 1.8rem;
  color: var(--color-accent);
  margin-bottom: 1rem;
  font-weight: 400;
  font-family: var(--font-body);
}

.location {
  font-size: 1.1rem;
  margin-bottom: 1.5rem;
  opacity: 0.8;
  font-style: italic;
}

.social-links {
  display: flex;
  gap: 1.5rem;
}

.social-link {
  font-size: 1.5rem;
  color: var(--color-dark);
  transition: all 0.3s ease;
  position: relative;
}

.social-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 2px;
  background: var(--color-dark);
  transform: scaleX(0);
  transition: transform 0.3s ease;
}

.social-link:hover::after {
  transform: scaleX(1);
}

@media (max-width: 1024px) {
  .header-content {
    max-width: 900px;
    gap: 3rem;
  }

  .profile-image {
    width: 250px;
    height: 250px;
  }

  h1 {
    font-size: 3rem;
  }
}

@media (max-width: 768px) {
  .header {
    padding: 4rem 0;
  }

  .header-content {
    flex-direction: column;
    text-align: center;
    gap: 2rem;
    max-width: 600px;
  }

  .text-content {
    align-items: center;
  }

  .profile-image {
    width: 200px;
    height: 200px;
  }

  h1 {
    font-size: 2.5rem;
  }

  .social-links {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .header {
    padding: 3rem 0;
  }

  .header-content {
    max-width: 100%;
    padding: 0 0.5rem;
  }

  .profile-image {
    width: 150px;
    height: 150px;
  }

  h1 {
    font-size: 2rem;
  }

  h2 {
    font-size: 1.4rem;
  }

  .location {
    font-size: 1rem;
  }
}
</style> 