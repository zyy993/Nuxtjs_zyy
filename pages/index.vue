<template>
  <div id="app">
    <Navbar />
    <main>
      <HeroSection />
      <AboutSection />
      <ProjectsSection />
      <ContactSection />
    </main>
    <footer class="footer">
      <p>
        &copy; <span>{{ currentYear }}</span>. Zyy993. All Rights Reserved.
      </p>
    </footer>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue';
import HeroSection from '~/components/HeroSection.vue';
import AboutSection from '~/components/AboutSection.vue';
import ProjectsSection from '~/components/ProjectsSection.vue';
import ContactSection from '~/components/ContactSection.vue';
import '@fortawesome/fontawesome-free/css/all.css';

export default {
  components: {
    Navbar,
    HeroSection,
    AboutSection,
    ProjectsSection,
    ContactSection
  },
  data() {
    return {
      currentYear: new Date().getFullYear()
    };
  }
};
</script>

<style>
/* Global styles for the entire application */

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1;
}

.footer {
  background-color: #161616;
  color: #ffffff;
  text-align: center;
  padding: 20px 0;
  box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.2);
}

.footer p {
  margin: 0;
  font-size: 1em;
}

.footer span {
  color: #fd8791; /* Secondary color */
}
</style>
