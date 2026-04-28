<template>
  <section id="education">
    <div class="container">
      <h2 class="section-title">학력</h2>
      <div class="edu-card">
        <div class="edu-icon">🎓</div>
        <div class="edu-info">
          <h3>국민대학교</h3>
          <p class="major">소프트웨어학부 소프트웨어학과</p>
          <p class="detail">Seoul, Korea</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.edu-card {
  display: flex;
  align-items: center;
  gap: 24px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 32px;
  max-width: 540px;
  transition: border-color 0.2s, transform 0.2s;
}

.edu-card:hover {
  border-color: var(--accent);
  transform: translateY(-4px);
}

.edu-icon {
  font-size: 3rem;
  flex-shrink: 0;
}

.edu-info h3 {
  font-size: 1.4rem;
  font-weight: 700;
  margin-bottom: 6px;
}

.major {
  color: var(--accent);
  font-size: 0.95rem;
  font-weight: 500;
  margin-bottom: 4px;
}

.detail {
  color: var(--text-muted);
  font-size: 0.875rem;
}
</style>
