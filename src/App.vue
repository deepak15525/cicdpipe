<script setup>
const stats = [
  { value: '6+', label: 'digital products' },
  { value: '3D', label: 'UX motion focus' },
  { value: '100%', label: 'brand-first thinking' },
]

const skills = [
  'Vue 3',
  'JavaScript',
  'TypeScript',
  'Product UI',
  'ERP UX',
  'React',
  'Node.js',
  'REST APIs',
  'Cloud',
  'Automation',
]

const projects = [
  {
    title: 'EOLAC',
    description: 'Smart logistics and shipping platform designed for scalability, faster booking, and clean operational visibility.',
    tag: 'Logistics',
    url: 'https://www.eolac.com/'
  },
  {
    title: 'EZ ChildTrack',
    description: 'Childcare management ecosystem with parent engagement, billing automation, and admin-friendly workflows.',
    tag: 'EdTech',
    url: 'https://www.ezchildtrack.com/'
  },
  {
    title: 'Infory',
    description: 'Health and fitness product experience focused on mobile engagement, conversion, and simplicity.',
    tag: 'HealthTech',
    url: 'https://www.infory.in/'
  },
  {
    title: 'Swift Food',
    description: 'Food-tech digital experience crafted to improve ordering flow, discoverability, and customer trust.',
    tag: 'Food Tech',
    url: 'https://www.swiftfood.com/'
  },
  {
    title: 'Aron Global',
    description: 'Premium B2B trading website built around credibility, global scale, and polished industrial storytelling.',
    tag: 'Global Trade',
    url: 'https://www.aronglobal.com/'
  },
  {
    title: 'The Presence 360',
    description: 'Enterprise ERP brand presence with strong storytelling, large product narratives, and conversion-focused structure.',
    tag: 'ERP',
    url: 'https://thepresence360.com/in/home'
  },
]

const principles = [
  'Product strategy',
  'Modern UX design',
  'Responsive interfaces',
  'Business-focused storytelling',
]

const tiltCard = (event) => {
  const card = event.currentTarget
  const rect = card.getBoundingClientRect()
  const x = event.clientX - rect.left
  const y = event.clientY - rect.top
  const rotateY = ((x / rect.width) - 0.5) * 24
  const rotateX = (0.5 - y / rect.height) * 24

  card.style.transform = `perspective(1400px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-8px)`
}

const resetCard = (event) => {
  event.currentTarget.style.transform = 'perspective(1400px) rotateX(0deg) rotateY(0deg) translateY(0px)'
}
</script>

<template>
  <div class="page-shell">
    <div class="background-grid"></div>
    <div class="orb orb-one"></div>
    <div class="orb orb-two"></div>
    <div class="orb orb-three"></div>

    <header class="topbar container">
      <div class="brand-wrap">
        <div class="brand-mark">D</div>
        <span>Deepak Jaiswal</span>
      </div>

      <nav class="nav-links">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>

      <a class="button ghost-button" href="https://www.linkedin.com/in/deepak-jaiswal-3bb9441a4" target="_blank" rel="noreferrer">
        LinkedIn
      </a>
    </header>

    <main class="container">
      <section class="hero">
        <div class="hero-copy">
          <p class="eyebrow">Product design • Engineering • Growth</p>
          <h1>Building premium digital experiences that move businesses forward.</h1>
          <p class="lead">
            I design and build modern products with a strong balance of user experience, clean front-end engineering,
            and business impact. My work helps brands look credible, feel memorable, and convert better.
          </p>

          <div class="cta-row">
            <a class="button primary-button" href="#projects">Explore work</a>
            <a class="button secondary-button" href="https://www.linkedin.com/in/deepak-jaiswal-3bb9441a4" target="_blank" rel="noreferrer">
              Connect on LinkedIn
            </a>
          </div>

          <div class="stat-row">
            <div v-for="item in stats" :key="item.label" class="stat-item">
              <strong>{{ item.value }}</strong>
              <span>{{ item.label }}</span>
            </div>
          </div>
        </div>

        <div class="hero-visual">
          <div class="visual-scene">
            <div class="floating-tag tag-1">UI Systems</div>
            <div class="floating-tag tag-2">Growth</div>
            <div class="floating-tag tag-3">3D UX</div>

            <div class="visual-card tilt-card" @pointermove="tiltCard" @pointerleave="resetCard">
              <div class="mini-badge">Available</div>
              <div class="profile-ring">
                <div class="profile-avatar">DJ</div>
              </div>
              <div class="card-meta">
                <span>Profile</span>
                <strong>Deepak Jaiswal</strong>
              </div>
              <div class="signal-bars">
                <span></span>
                <span></span>
                <span></span>
                <span></span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="trust-strip">
        <div class="strip-label">Project influence</div>
        <div class="strip-items">
          <span>EOLAC</span>
          <span>EZChildTrack</span>
          <span>Infory</span>
          <span>Swift Food</span>
          <span>Aron Global</span>
          <span>Presence360</span>
        </div>
      </section>

      <section id="about" class="info-grid">
        <div class="panel glass-panel about-panel">
          <p class="section-tag">About</p>
          <h2>Designing clean interfaces and practical product systems.</h2>
          <p>
            I create experiences that feel premium, perform smoothly, and communicate trust. From product ideas to polished interfaces,
            I focus on clarity, conversion, and consistency across every touchpoint.
          </p>
        </div>

        <div class="panel glass-panel focus-panel">
          <p class="section-tag">Approach</p>
          <ul>
            <li v-for="item in principles" :key="item">{{ item }}</li>
          </ul>
        </div>
      </section>

      <section id="skills" class="skills-section">
        <div class="section-heading">
          <p class="section-tag">Core strengths</p>
          <h2>Technology and creative capability built for modern businesses.</h2>
        </div>

        <div class="skills-grid">
          <div v-for="skill in skills" :key="skill" class="skill-pill tilt-card" @pointermove="tiltCard" @pointerleave="resetCard">
            {{ skill }}
          </div>
        </div>
      </section>

      <section id="projects" class="projects-section">
        <div class="section-heading">
          <p class="section-tag">Selected work</p>
          <h2>Real-world products built with clarity, structure, and momentum.</h2>
        </div>

        <div class="project-grid">
          <article
            v-for="project in projects"
            :key="project.title"
            class="project-card tilt-card"
            @pointermove="tiltCard"
            @pointerleave="resetCard"
          >
            <span class="project-tag">{{ project.tag }}</span>
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <a class="project-link" :href="project.url" target="_blank" rel="noreferrer">Visit website</a>
          </article>
        </div>
      </section>

      <section class="timeline-section">
        <div class="section-heading">
          <p class="section-tag">Professional journey</p>
          <h2>From interface building to end-to-end product execution.</h2>
        </div>

        <div class="timeline">
          <div v-for="item in [{ period: '2024 — Present', role: 'Product-focused engineer', detail: 'Designing growth-driven digital experiences with a sharp eye on UX quality, modern front-end performance, and business clarity.' }, { period: '2022 — 2024', role: 'Digital experience builder', detail: 'Delivered user-centric interfaces and product surfaces for business, SaaS, and service-oriented brands.' }, { period: '2020 — 2022', role: 'Frontend problem solver', detail: 'Collaborated across design and engineering to turn concepts into polished, reliable digital experiences.' } ]" :key="item.period" class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-content">
              <span>{{ item.period }}</span>
              <h3>{{ item.role }}</h3>
              <p>{{ item.detail }}</p>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer id="contact" class="contact-bar container">
      <div>
        <p class="section-tag">Let’s build</p>
        <h2>Open to product, design, and engineering opportunities.</h2>
      </div>

      <div class="contact-actions">
        <a class="button primary-button" href="https://www.linkedin.com/in/deepak-jaiswal-3bb9441a4" target="_blank" rel="noreferrer">
          Connect on LinkedIn
        </a>
      </div>
    </footer>
  </div>
</template>
