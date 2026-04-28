<template>
  <footer>
    <div class="container footer-inner">
      <p class="copy">© 2026 · Built with <span class="heart">Vue.js</span></p>
      <a href="#hero" class="back-top">↑ 맨 위로</a>
    </div>
  </footer>
</template>

<style scoped>
footer {
  border-top: 1px solid var(--border);
  padding: 32px 0;
}

.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
}

.copy {
  color: var(--text-muted);
  font-size: 0.875rem;
}

.heart {
  color: var(--accent-green);
  font-weight: 600;
}

.back-top {
  color: var(--text-muted);
  font-size: 0.875rem;
  transition: color 0.2s;
}

.back-top:hover {
  color: var(--accent);
}
</style>
