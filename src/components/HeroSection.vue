<template>
  <section id="hero" class="hero">
    <div class="container hero-inner">
      <div class="hero-text fade-in">
        <p class="greeting">안녕하세요 👋</p>
        <h1 class="name">백엔드 개발자<br><span class="highlight">포트폴리오</span></h1>
        <p class="bio">
          금융·의료 도메인 시스템 구축 및 유지보수 경험을 보유한 백엔드 개발자입니다.<br>
          안정적이고 확장 가능한 서버 아키텍처 설계와 레거시 시스템 운영에 강점이 있습니다.
        </p>
        <div class="cta-group">
          <a href="#projects" class="btn-primary">프로젝트 보기</a>
          <a href="#skills" class="btn-ghost">기술 스택</a>
        </div>
      </div>
      <div class="hero-deco" aria-hidden="true">
        <div class="profile-wrap">
          <img src="../assets/hero.png" alt="프로필 이미지" class="profile-img" />
        </div>
      </div>
    </div>
    <div class="hero-bg" aria-hidden="true">
      <div class="orb orb1" />
      <div class="orb orb2" />
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding-top: 80px;
}

.hero-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: center;
}

.hero-text {
  animation-delay: 0.1s;
}

.greeting {
  color: var(--accent);
  font-size: 1.1rem;
  font-weight: 500;
  margin-bottom: 16px;
}

.name {
  font-size: clamp(2.2rem, 5vw, 3.2rem);
  font-weight: 800;
  line-height: 1.2;
  margin-bottom: 20px;
  letter-spacing: -1px;
}

.highlight {
  background: linear-gradient(135deg, var(--accent), var(--accent-purple));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.bio {
  color: var(--text-muted);
  font-size: 1rem;
  line-height: 1.8;
  margin-bottom: 36px;
  max-width: 480px;
}

.cta-group {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}

.btn-primary {
  padding: 12px 28px;
  background: var(--accent);
  color: #0d1117;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.95rem;
  transition: opacity 0.2s, transform 0.2s;
}

.btn-primary:hover {
  opacity: 0.85;
  transform: translateY(-2px);
}

.btn-ghost {
  padding: 12px 28px;
  border: 1px solid var(--border);
  color: var(--text);
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.95rem;
  transition: border-color 0.2s, transform 0.2s;
}

.btn-ghost:hover {
  border-color: var(--accent);
  transform: translateY(-2px);
}

/* Profile image */
.profile-wrap {
  display: flex;
  justify-content: center;
  align-items: center;
  animation: fadeInUp 0.7s 0.3s ease both;
}

.profile-img {
  width: 100%;
  max-width: 360px;
  height: auto;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  display: block;
}

/* Background orbs */
.hero-bg {
  position: absolute;
  inset: 0;
  pointer-events: none;
  z-index: -1;
}

.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);
  opacity: 0.12;
}

.orb1 {
  width: 500px;
  height: 500px;
  background: var(--accent);
  top: -100px;
  right: -100px;
}

.orb2 {
  width: 400px;
  height: 400px;
  background: var(--accent-purple);
  bottom: -100px;
  left: -50px;
}

@media (max-width: 768px) {
  .hero-inner {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .hero-deco {
    order: -1;
  }
}
</style>
