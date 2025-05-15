<script>
import Header from './components/Header.vue'
import Skills from './components/Skills.vue'
import Experience from './components/Experience.vue'

export default {
  name: 'App',
  components: {
    Header,
    Skills,
    Experience
  }
}
</script>

<template>
  <div class="app">
    <div class="noise-overlay"></div>
    <Header />
    <Skills />
    <Experience />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Crimson+Text:wght@400;600;700&family=Space+Mono:wght@400;700&display=swap');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css');

:root {
  --color-dark: #f5f5f5;
  --color-light: #0a0a0a;
  --color-accent: #cccccc;
  --font-heading: 'Crimson Text', serif;
  --font-body: 'Space Mono', monospace;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: var(--font-body);
  line-height: 1.6;
  color: var(--color-dark);
  background-color: var(--color-light);
}

.app {
  min-height: 100vh;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}

.noise-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 400 400' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
  opacity: 0.1;
  pointer-events: none;
  z-index: 1;
  mix-blend-mode: difference;
}

a {
  text-decoration: none;
  color: inherit;
  transition: all 0.3s ease;
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-heading);
  font-weight: 700;
  line-height: 1.3;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1.5rem;
  position: relative;
  z-index: 2;
}

section {
  width: 100%;
  display: flex;
  justify-content: center;
}

@media (max-width: 1024px) {
  .container {
    max-width: 90%;
  }
}

@media (max-width: 768px) {
  html {
    font-size: 14px;
  }
  .container {
    max-width: 95%;
    padding: 0 1rem;
  }
}

@media (max-width: 480px) {
  html {
    font-size: 12px;
  }
  .container {
    max-width: 100%;
    padding: 0 0.8rem;
  }
}
</style>
