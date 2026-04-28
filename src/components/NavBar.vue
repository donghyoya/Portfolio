<template>
  <nav class="navbar" :class="{ scrolled: isScrolled }">
    <div class="container nav-inner">
      <a href="#hero" class="logo">Portfolio</a>
      <ul class="nav-links">
        <li><a href="#skills" @click="close">기술 스택</a></li>
        <li><a href="#projects" @click="close">프로젝트</a></li>
        <li><a href="#education" @click="close">학력</a></li>
      </ul>
      <button class="hamburger" @click="menuOpen = !menuOpen" :class="{ open: menuOpen }">
        <span /><span /><span />
      </button>
    </div>
    <div class="mobile-menu" :class="{ open: menuOpen }">
      <a href="#skills" @click="close">기술 스택</a>
      <a href="#projects" @click="close">프로젝트</a>
      <a href="#education" @click="close">학력</a>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const menuOpen = ref(false)

function onScroll() {
  isScrolled.value = window.scrollY > 40
}

function close() {
  menuOpen.value = false
}

onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  transition: background 0.3s, box-shadow 0.3s;
  padding: 16px 0;
}

.navbar.scrolled {
  background: rgba(13, 17, 23, 0.95);
  backdrop-filter: blur(12px);
  box-shadow: 0 1px 0 var(--border);
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--accent);
  letter-spacing: -0.5px;
}

.nav-links {
  display: flex;
  gap: 32px;
  list-style: none;
}

.nav-links a {
  color: var(--text-muted);
  font-size: 0.9rem;
  transition: color 0.2s;
}

.nav-links a:hover {
  color: var(--text);
}

.hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
}

.hamburger span {
  display: block;
  width: 22px;
  height: 2px;
  background: var(--text);
  border-radius: 2px;
  transition: all 0.3s;
}

.hamburger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
.hamburger.open span:nth-child(2) { opacity: 0; }
.hamburger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

.mobile-menu {
  display: none;
  flex-direction: column;
  gap: 16px;
  padding: 16px 24px 20px;
  background: rgba(13, 17, 23, 0.98);
}

.mobile-menu a {
  color: var(--text-muted);
  font-size: 1rem;
}

@media (max-width: 640px) {
  .nav-links { display: none; }
  .hamburger { display: flex; }
  .mobile-menu.open { display: flex; }
}
</style>
