<template>
  <NavBar />
  <main>
    <HeroSection />
    <CareerSection />
    <SkillsSection />
    <ProjectsSection />
    <EducationSection />
  </main>
  <FooterSection />
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import CareerSection from './components/CareerSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import EducationSection from './components/EducationSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>
