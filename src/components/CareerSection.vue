<template>
  <section id="career">
    <div class="container">
      <h2 class="section-title">경력</h2>
      <div class="timeline">
        <div v-for="(item, i) in careers" :key="i" class="timeline-item">
          <div class="timeline-left">
            <span class="period">{{ item.period }}</span>
            <span class="duration">{{ item.duration }}</span>
          </div>
          <div class="timeline-connector">
            <div class="dot" :class="{ current: item.current }" />
            <div class="line" v-if="i < careers.length - 1" />
          </div>
          <div class="timeline-card" :class="{ current: item.current }">
            <div class="card-head">
              <div>
                <h3 class="company">{{ item.company }}</h3>
                <p class="role">{{ item.role }}</p>
              </div>
              <span v-if="item.current" class="badge-current">재직 중</span>
            </div>
            <p class="desc">{{ item.desc }}</p>
            <div class="tags">
              <span v-for="tag in item.tags" :key="tag" class="tech-tag">{{ tag }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const careers = [
  {
    company: 'NZERO',
    role: '백엔드 개발자',
    period: '2026.04 ~ 현재',
    duration: '재직 중',
    current: true,
    desc: '백엔드 시스템 개발 및 운영. 안정적인 서비스 제공을 위한 서버 아키텍처 설계 및 인프라 관리.',
    tags: ['Spring Boot', 'Java', 'Docker', 'Vue.js'],
  },
  {
    company: '오상테크놀로지',
    role: '백엔드 개발자',
    period: '2024.03 ~ 2026.04',
    duration: '2년 2개월',
    current: false,
    desc: '금융·의료·공공 도메인 시스템 구축 및 유지보수. 우리금융저축은행, 페퍼저축은행, 경희의료원 등 다수 고객사 프로젝트 참여.',
    tags: ['Java', 'Spring Boot', 'MySQL', 'MariaDB', 'PostgreSQL', 'Redis', 'JEUS', 'Docker'],
  },
]
</script>

<style scoped>
.timeline {
  display: flex;
  flex-direction: column;
  gap: 0;
}

.timeline-item {
  display: grid;
  grid-template-columns: 140px 32px 1fr;
  gap: 0 16px;
  align-items: start;
}

.timeline-left {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  padding-top: 20px;
  gap: 4px;
}

.period {
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--text-muted);
  text-align: right;
  line-height: 1.4;
}

.duration {
  font-size: 0.72rem;
  color: var(--text-muted);
  opacity: 0.6;
}

.timeline-connector {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 24px;
}

.dot {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: var(--border);
  border: 2px solid var(--bg);
  flex-shrink: 0;
  z-index: 1;
  transition: background 0.2s;
}

.dot.current {
  background: var(--accent);
  box-shadow: 0 0 0 4px rgba(88, 166, 255, 0.2);
}

.line {
  width: 2px;
  flex: 1;
  min-height: 32px;
  background: var(--border);
  margin-top: 4px;
}

.timeline-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 20px 24px;
  margin-bottom: 20px;
  transition: border-color 0.2s, transform 0.2s;
}

.timeline-card:hover {
  transform: translateX(4px);
  border-color: var(--accent);
}

.timeline-card.current {
  border-color: rgba(88, 166, 255, 0.4);
  background: rgba(88, 166, 255, 0.03);
}

.card-head {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 10px;
  gap: 12px;
}

.company {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 3px;
}

.role {
  font-size: 0.85rem;
  color: var(--accent);
  font-weight: 500;
}

.badge-current {
  flex-shrink: 0;
  padding: 3px 10px;
  background: rgba(88, 166, 255, 0.15);
  color: var(--accent);
  border: 1px solid rgba(88, 166, 255, 0.3);
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 600;
}

.desc {
  color: var(--text-muted);
  font-size: 0.875rem;
  line-height: 1.7;
  margin-bottom: 14px;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.tech-tag {
  padding: 3px 10px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid var(--border);
  border-radius: 6px;
  font-size: 0.75rem;
  color: var(--text-muted);
  font-family: 'Cascadia Code', 'Fira Code', monospace;
}

@media (max-width: 580px) {
  .timeline-item {
    grid-template-columns: 0 28px 1fr;
  }

  .timeline-left {
    display: none;
  }

  .period-mobile {
    display: block;
  }
}
</style>
