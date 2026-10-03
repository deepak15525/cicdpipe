<script setup>
import SectionHeader from './components/SectionHeader.vue'
import SkillPill from './components/SkillPill.vue'
import ProjectCard from './components/ProjectCard.vue'
import CapabilityCard from './components/CapabilityCard.vue'

const stats = [
    { value: '8+', label: 'full-stack solutions' },
    { value: '100%', label: 'product execution' },
    { value: 'AWS/Azure', label: 'cloud delivery' },
]

const skills = [
    'Node.js',
    'Laravel',
    'Vue.js',
    'Nuxt.js',
    '.NET Core',
    'AWS',
    'Azure',
    'DevOps',
    'REST APIs',
    'Cloud Architecture',
]

const capabilities = [
    {
        title: 'Frontend Engineering',
        description: 'Designing modern, responsive, and conversion-focused user experiences using Vue.js, Nuxt.js, and component-first architecture.',
        tags: ['Vue.js', 'Nuxt.js', 'UI Systems', 'Performance']
    },
    {
        title: 'Backend & APIs',
        description: 'Building reliable business logic, integrations, and APIs in Node.js, Laravel, and .NET Core for scalable digital products.',
        tags: ['Node.js', 'Laravel', '.NET Core', 'REST APIs']
    },
    {
        title: 'Cloud & DevOps',
        description: 'Delivering secure, production-ready deployments with AWS, Azure, CI/CD pipelines, monitoring, and infrastructure automation.',
        tags: ['AWS', 'Azure', 'DevOps', 'CI/CD']
    },
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
        title: 'Nimeya.ai',
        description: 'Insurance intelligence platform blending deep sector expertise with AI to benchmark products, support regulatory decisions, and turn complex operational data into clearer business actions.',
        tag: 'Insurance AI',
        url: 'https://nimeya.ai/'
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
    'Full-stack product development',
    'Component-based architecture',
    'Cloud-native deployment',
    'DevOps and automation',
]


const profileImage = 'https://media.licdn.com/dms/image/v2/C5103AQGhUFEVSFapbg/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1583940133968?e=1792627200&v=beta&t=GvKb-G4iUbtwA3-bcEmSgKw_m88jOunMTQ6E8AGLau4'

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

const parallaxScene = (event) => {
    const scene = event.currentTarget
    const rect = scene.getBoundingClientRect()
    const x = (event.clientX - rect.left) / rect.width - 0.5
    const y = (event.clientY - rect.top) / rect.height - 0.5

    scene.style.transform = `translate3d(${(x * 10).toFixed(2)}px, ${(y * 10).toFixed(2)}px, 0) rotateX(${(-y * 6).toFixed(2)}deg) rotateY(${(x * 8).toFixed(2)}deg)`
}

const resetScene = (event) => {
    event.currentTarget.style.transform = 'translate3d(0, 0, 0) rotateX(0deg) rotateY(0deg)'
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
                <a href="#capabilities">Capabilities</a>
                <a href="#skills">Skills</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </nav>

            <a class="button ghost-button" href="https://www.linkedin.com/in/deepak-jaiswal-3bb9441a4" target="_blank"
                rel="noreferrer">
                LinkedIn
            </a>
        </header>

        <main class="container">
            <section class="hero">
                <div class="hero-copy">
                    <div class="marquee-shell" aria-label="Technology focus areas">
                        <div class="marquee-track">
                            <span>Solution Design</span>
                            <span>Cloud Delivery</span>
                            <span>Product Engineering</span>
                            <span>Solution Design</span>
                            <span>Cloud Delivery</span>
                            <span>Product Engineering</span>
                        </div>
                    </div>
                    <p class="eyebrow">Senior Software Analyst</p>
                    <h1 class="hero-title">Modern products. Faster execution. Better business outcomes.</h1>
                    <p class="lead">
                        I design and deliver scalable digital platforms that connect customer experience, cloud
                        architecture, and business growth—using Vue.js, Nuxt.js, Node.js, Laravel, .NET Core, AWS,
                        Azure, and DevOps.
                    </p>

                    <div class="cta-row">
                        <a class="button primary-button" href="#projects">Explore work</a>
                        <a class="button secondary-button" href="https://www.linkedin.com/in/deepak-jaiswal-3bb9441a4"
                            target="_blank" rel="noreferrer">
                            Connect on LinkedIn
                        </a>
                    </div>

                    <div class="stack-strip">
                        <span v-for="tech in skills.slice(0, 8)" :key="tech">{{ tech }}</span>
                    </div>

                    <div class="stat-row">
                        <div v-for="item in stats" :key="item.label" class="stat-item">
                            <strong>{{ item.value }}</strong>
                            <span>{{ item.label }}</span>
                        </div>
                    </div>
                </div>

                <div class="hero-visual">
                    <div class="visual-scene" @pointermove="parallaxScene" @pointerleave="resetScene">
                        <div class="floating-tag tag-1">UI Systems</div>
                        <div class="floating-tag tag-2">Cloud</div>
                        <div class="floating-tag tag-3">DevOps</div>

                        <div class="visual-card tilt-card" @pointermove="tiltCard" @pointerleave="resetCard">
                            <div class="mini-badge">Available</div>
                            <div class="profile-ring">
                                <img class="profile-photo" :src="profileImage" alt="Deepak Jaiswal portrait" />
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
                    <span>Nimeya.ai</span>
                    <span>Aron Global</span>
                    <span>Presence360</span>
                </div>
            </section>

            <section id="about" class="info-grid">
                <div class="panel glass-panel about-panel">
                    <p class="section-tag">About</p>
                    <h2>Senior-level software thinking that connects business goals with engineering execution.</h2>
                    <p>
                        I work at the intersection of product thinking, system design, and delivery leadership. My focus
                        is
                        on building secure, scalable, and user-centered platforms that support business growth while
                        maintaining technical quality, performance, and long-term maintainability.
                    </p>
                </div>

                <div class="panel glass-panel focus-panel">
                    <p class="section-tag">Approach</p>
                    <ul>
                        <li v-for="item in principles" :key="item">{{ item }}</li>
                    </ul>
                </div>
            </section>

            <section id="capabilities" class="capability-section">
                <SectionHeader tag="Capabilities"
                    title="A component-based delivery model for product, platform, and cloud." />
                <div class="capability-grid">
                    <CapabilityCard v-for="item in capabilities" :key="item.title" :title="item.title"
                        :description="item.description" :tags="item.tags" />
                </div>
            </section>

            <section id="skills" class="skills-section">
                <SectionHeader tag="Core strengths" title="Technology stack built for modern product delivery." />

                <div class="skills-grid">
                    <SkillPill v-for="skill in skills" :key="skill" :label="skill" @tilt="tiltCard"
                        @reset="resetCard" />
                </div>
            </section>

            <section id="projects" class="projects-section">
                <SectionHeader tag="Selected work"
                    title="Real-world products built with clarity, structure, and momentum." />

                <div class="project-grid">
                    <ProjectCard v-for="project in projects" :key="project.title" :project="project" @tilt="tiltCard"
                        @reset="resetCard" />
                </div>
            </section>

            <section class="timeline-section">
                <SectionHeader tag="Professional journey"
                    title="From interface building to end-to-end product execution." />

                <div class="timeline">
                    <div v-for="item in [{ period: '2024 — Present', role: 'Full-stack product engineer', detail: 'Building scalable frontend, backend, and deployment systems with a sharp focus on product quality, architecture, and cloud reliability.' }, { period: '2022 — 2024', role: 'Digital product & platform builder', detail: 'Delivered user-centric interfaces, APIs, and business-driven systems for SaaS, service, and growth-focused brands.' }, { period: '2020 — 2022', role: 'Frontend and solution engineer', detail: 'Turned product concepts into reliable digital experiences across design, development, and release workflows.' }]"
                        :key="item.period" class="timeline-item">
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
                <h2>Available for product, platform, and cloud transformation work.</h2>
            </div>

            <div class="contact-actions">
                <a class="button primary-button" href="https://www.linkedin.com/in/deepak-jaiswal-3bb9441a4"
                    target="_blank" rel="noreferrer">
                    Connect on LinkedIn
                </a>
            </div>
        </footer>
    </div>
</template>
