<template>
  <section id="projects" class="projects-section">
    <div class="container">
      <h2 class="section-title"><br><img src="data:image/jpg;base64,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" style="max-width: 100% !important; height: auto !important; border-radius: 4px !important; display: inline-block !important; vertical-align: middle !important;"><br>참여 프로젝트</h2>
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
