<template>
  <section id="projects" class="projects-section">
    <div class="container">
      <h2 class="section-title">참여 프로젝트</h2>
      <div class="projects-grid">
        <article v-for="(project, i) in projects" :key="i" class="project-card">
          <div class="card-top">
            <span class="domain-badge" :class="project.domain">{{ domainLabel[project.domain] }}</span>
            <h3 class="project-name">{{ project.name }}</h3>
            <p class="project-desc">{{ project.desc }}</p>
          </div>
          <div class="card-footer">
            <span v-for="tag in project.tags" :key="tag" class="tech-tag">{{ tag }}</span>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
const domainLabel = {
  finance: '금융',
  medical: '의료',
  public: '공공',
}

const projects = [
  {
    name: '우리금융저축은행',
    desc: '우리금융저축은행 핵심 업무 시스템 구축 및 운영 유지보수. 안정적인 금융 서비스 제공을 위한 서버 환경 관리 및 장애 대응.',
    domain: 'finance',
    tags: ['Spring Boot', 'Java', 'Oracle', 'JEUS', 'Tmax'],
  },
  {
    name: '페퍼저축은행',
    desc: '페퍼저축은행 업무 시스템 구축 및 유지보수. 금융 트랜잭션 안정성 확보 및 시스템 고도화.',
    domain: 'finance',
    tags: ['Spring', 'Java', 'MySQL', 'Tomcat'],
  },
  {
    name: '임업진흥원',
    desc: '국립 임업진흥원 정보 시스템 구축 및 유지보수. 공공기관 업무 시스템 개발 및 운영.',
    domain: 'public',
    tags: ['Spring Boot', 'Java', 'MariaDB', 'Docker'],
  },
  {
    name: '창원파티마병원',
    desc: '창원파티마병원 의료 정보 시스템 구축 및 유지보수. 병원 업무 흐름에 맞춘 안정적인 시스템 운영.',
    domain: 'medical',
    tags: ['Spring', 'JSP', 'Oracle', 'Tomcat'],
  },
  {
    name: '이대목동병원',
    desc: '이화여대 목동병원 의료 시스템 구축 및 유지보수. 의료 데이터 관리 및 병원 내부 시스템 연동.',
    domain: 'medical',
    tags: ['Spring Boot', 'Java', 'PostgreSQL', 'Docker'],
  },
  {
    name: '이대서울병원',
    desc: '이화여대 서울병원 시스템 구축 및 유지보수. 의료 서비스 향상을 위한 백엔드 개발 및 운영.',
    domain: 'medical',
    tags: ['Spring Boot', 'Vue.js', 'MariaDB'],
  },
  {
    name: '이대병원 서버 이관',
    desc: '이화여대 산하 병원 레거시 서버 신규 인프라 이관 프로젝트. 무중단 마이그레이션 계획 수립 및 실행.',
    domain: 'medical',
    tags: ['Docker Compose', 'Rocky Linux', 'Redis', 'AWS Linux'],
  },
  {
    name: '경희의료원',
    desc: '경희의료원 의료 정보 시스템 구축 및 유지보수. 대용량 의료 데이터 처리 및 시스템 안정화.',
    domain: 'medical',
    tags: ['Spring Boot', 'Java', 'MySQL', 'Redis'],
  },
  {
    name: '강동경희대병원',
    desc: '강동경희대병원 시스템 구축 및 유지보수. 병원 시스템 현대화 및 인프라 개선.',
    domain: 'medical',
    tags: ['Spring', 'FastAPI', 'PostgreSQL', 'Docker'],
  },
]
</script>

<style scoped>
.projects-section {
  background: rgba(255, 255, 255, 0.01);
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 20px;
}

.project-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 20px;
  transition: border-color 0.2s, transform 0.2s, box-shadow 0.2s;
  cursor: default;
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow);
  border-color: var(--accent);
}

.domain-badge {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 999px;
  font-size: 0.75rem;
  font-weight: 600;
  margin-bottom: 12px;
}

.domain-badge.finance {
  background: rgba(88, 166, 255, 0.15);
  color: var(--accent);
  border: 1px solid rgba(88, 166, 255, 0.3);
}

.domain-badge.medical {
  background: rgba(63, 185, 80, 0.15);
  color: var(--accent-green);
  border: 1px solid rgba(63, 185, 80, 0.3);
}

.domain-badge.public {
  background: rgba(240, 136, 62, 0.15);
  color: var(--accent-orange);
  border: 1px solid rgba(240, 136, 62, 0.3);
}

.project-name {
  font-size: 1.15rem;
  font-weight: 700;
  margin-bottom: 10px;
  line-height: 1.3;
}

.project-desc {
  color: var(--text-muted);
  font-size: 0.875rem;
  line-height: 1.7;
}

.card-footer {
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
</style>
