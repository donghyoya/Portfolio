<template>
  <section id="skills">
    <div class="container">
      <h2 class="section-title">기술 스택</h2>
      <div class="skill-grid">
        <div v-for="group in skillGroups" :key="group.label" class="skill-card">
          <div class="skill-card-header">
            <span class="skill-icon">{{ group.icon }}</span>
            <h3>{{ group.label }}</h3>
          </div>
          <div class="tags">
            <span
              v-for="skill in group.skills"
              :key="skill"
              class="tag"
              :style="{ '--tag-color': group.color }"
            >{{ skill }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const skillGroups = [
  {
    label: '백엔드',
    icon: '⚙️',
    color: '#58a6ff',
    skills: ['Java', 'Spring', 'Spring Boot', 'Python', 'FastAPI'],
  },
  {
    label: '데이터베이스',
    icon: '🗄️',
    color: '#3fb950',
    skills: ['MySQL', 'MariaDB', 'PostgreSQL', 'Redis'],
  },
  {
    label: '프론트엔드',
    icon: '🖥️',
    color: '#bc8cff',
    skills: ['Vue.js', 'JSP'],
  },
  {
    label: '서버 / 미들웨어',
    icon: '🖧',
    color: '#f0883e',
    skills: ['Tomcat', 'JEUS', 'Tmax'],
  },
  {
    label: '인프라 / DevOps',
    icon: '🐳',
    color: '#ff7b72',
    skills: ['Docker', 'Docker Compose', 'Rocky Linux', 'AWS Linux'],
  },
]
</script>

<style scoped>
.skill-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

.skill-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  transition: border-color 0.2s, transform 0.2s;
}

.skill-card:hover {
  border-color: var(--accent);
  transform: translateY(-4px);
}

.skill-card-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 16px;
}

.skill-icon {
  font-size: 1.4rem;
}

.skill-card-header h3 {
  font-size: 1rem;
  font-weight: 600;
  color: var(--text-muted);
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.tag {
  padding: 5px 12px;
  border-radius: 999px;
  font-size: 0.82rem;
  font-weight: 500;
  background: color-mix(in srgb, var(--tag-color) 15%, transparent);
  color: var(--tag-color);
  border: 1px solid color-mix(in srgb, var(--tag-color) 30%, transparent);
  transition: background 0.2s;
}

.tag:hover {
  background: color-mix(in srgb, var(--tag-color) 25%, transparent);
}
</style>
