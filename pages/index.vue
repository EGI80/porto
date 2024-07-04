<template>
  <div>
    <Navbar />
    <HeroSection />
    <AboutSection />
    <ProjectsSection />
    <ContactSection />
    <Footer />
    
  </div>
</template>

<script>
import HeroSection from '~/components/HeroSection.vue';
import AboutSection from '~/components/AboutSection.vue';
import ProjectsSection from '~/components/ProjectsSection.vue';
import ContactSection from '~/components/ContactSection.vue';
import Navbar from '~/components/Navbar.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    HeroSection,
    AboutSection,
    ProjectsSection,
    ContactSection,
    Navbar,
    Footer,
  }
}
</script>

<style scoped>
/* Anda dapat menambahkan gaya khusus untuk halaman ini di sini */
</style>
