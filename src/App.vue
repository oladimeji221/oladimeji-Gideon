<script setup>
import { onMounted, onUnmounted, ref } from 'vue'
import portrait from '../assets/img/aboout-me.png'
import techcareImage from '../assets/img/portfolio/techcare.png'
import daraImage from '../assets/img/portfolio/dara-onanuga.jpg'
import geoplotImage from '../assets/img/portfolio/geoplot.png'
import jfroyaleImage from '../assets/img/portfolio/jfroyale.png'
import kdImage from '../assets/img/portfolio/kd_xchange.png'
import wealthImage from '../assets/img/portfolio/babywealth.png'
import retrofitImage from '../assets/img/portfolio/retrofit.png'
import grameJohnsImage from '../assets/img/portfolio/gramejohns.png'
import gatunImage from '../assets/img/portfolio/gatunsecurity.png'
import primeShieldImage from '../assets/img/portfolio/primeshieldcare.png'
import birthdayImage from '../assets/img/portfolio/birthday.png'
import moedImage from '../assets/img/apps/moed.jpeg'
import bookamiaImage from '../assets/img/apps/bookamia.jpeg'
import bookamiaSplashImage from '../assets/img/apps/bookamia_splash.jpeg'
import vendorDashboardImage from '../assets/img/apps/vendor_dashboard.jpeg'
import bizTidyImage from '../assets/img/apps/biztidy.png'

const menuOpen = ref(false)
const scrolled = ref(false)

const projects = [
  {
    name: 'TechCare',
    number: '01',
    type: 'Health dashboard',
    blurb: 'A focused clinical dashboard that turns patient health data into clear, usable insights.',
    tags: ['Dashboard', 'Data UI', 'Frontend'],
    image: techcareImage,
    url: 'https://oladimeji221.github.io/TechCare/',
    tone: 'mint',
  },
  {
    name: 'Dara Onanuga',
    number: '02',
    type: 'Creative portfolio',
    blurb: 'A cinematic portfolio experience for a creative director and visual storyteller, designed to let the work take centre stage.',
    tags: ['Vue.js', 'Portfolio', 'Creative UI'],
    image: daraImage,
    url: 'https://www.daraonanuga.com/',
    tone: 'violet',
  },
  {
    name: 'Geoplot Resources',
    number: '03',
    type: 'Business platform',
    blurb: 'A credible digital home for a construction and real-estate services company.',
    tags: ['Business', 'Web Design', 'Development'],
    image: geoplotImage,
    url: 'http://geoplotresources.com/',
    tone: 'sand',
  },
  {
    name: 'JF Royale',
    number: '04',
    type: 'Logistics website',
    blurb: 'A modern, direct service experience built to make a logistics company easier to trust.',
    tags: ['Logistics', 'Revamp', 'Frontend'],
    image: jfroyaleImage,
    url: 'https://oladimeji221.github.io/jfroyale/',
    tone: 'coral',
  },
]

const archiveProjects = [
  {
    name: 'Gatun Security',
    type: 'Security services platform',
    image: gatunImage,
    url: 'https://gatunsecurity.com/',
    description: 'A comprehensive service platform covering corporate security, retail protection, CCTV monitoring and rapid response.',
  },
  {
    name: 'Prime Shield Care',
    type: 'Care & recruitment platform',
    image: primeShieldImage,
    url: 'https://primeshieldcare.co.uk/',
    description: 'A multi-service UK platform for healthcare staffing, professional cleaning and logistics solutions.',
  },
  {
    name: 'Mummy @ 70',
    type: 'Birthday celebration website',
    image: birthdayImage,
    url: null,
    description: 'A warm commemorative website for sharing birthday wishes, memories and a family photo gallery.',
  },
  {
    name: 'KD Xchange',
    type: 'Fintech landing page',
    image: kdImage,
    url: 'https://oladimeji221.github.io/kdxchange-landing-page/',
    description: 'A responsive product experience for exchanging cryptocurrency and digital assets.',
  },
  {
    name: 'BabyWealth Xchange',
    type: 'Digital assets platform',
    image: wealthImage,
    url: 'https://oladimeji221.github.io/BabyWealthXchange/',
    description: 'A conversion-focused website for cryptocurrency and gift-card services.',
  },
  {
    name: 'Retrofit Coordination',
    type: 'Business website',
    image: retrofitImage,
    url: 'https://oladimeji221.github.io/Retrofit-services/',
    description: 'A refreshed web presence that makes the company’s services easier to understand.',
  },
  {
    name: 'GrameJohns System',
    type: 'Electrical services',
    image: grameJohnsImage,
    url: 'https://gramejohnsystems.com/',
    description: 'A professional service website for an electrical solutions business.',
  },
]

const capabilities = [
  { mark: '01', title: 'Product frontends', text: 'Responsive interfaces with Vue, React, JavaScript and thoughtful interaction design.' },
  { mark: '02', title: 'Backend systems', text: 'APIs, business logic and database-backed applications built with Laravel and PHP.' },
  { mark: '03', title: 'Mobile apps', text: 'Cross-platform iOS and Android experiences built with React Native.' },
]

const stack = ['Vue.js', 'React', 'React Native', 'JavaScript', 'Laravel', 'PHP', 'Livewire', 'Tailwind CSS', 'WordPress', 'REST APIs']

const experience = [
  {
    period: 'Sep 2023 — Present',
    company: 'ECR Technology Services',
    role: 'Fullstack Developer & Frontend Tutor',
    location: 'Umuahia, Abia',
    summary: 'Building web experiences and helping 50+ students turn HTML, CSS and JavaScript fundamentals into practical, well-structured projects.',
  },
  {
    period: 'Dec 2016 — May 2017',
    company: 'Oceaneering Technology Services',
    role: 'Junior Web Developer',
    location: 'Lagos, Nigeria',
    summary: 'Developed responsive WordPress experiences, collaborated across disciplines, and tested and debugged client web applications.',
  },
]

function onScroll() {
  scrolled.value = window.scrollY > 24
}

onMounted(() => {
  window.addEventListener('scroll', onScroll, { passive: true })
  onScroll()
})
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<template>
  <div class="site-shell">
    <header :class="{ scrolled }">
      <a class="brand" href="#top" aria-label="Gideon home">
        <span>G</span><span class="brand-dot"></span>
      </a>
      <nav :class="{ open: menuOpen }" aria-label="Main navigation">
        <a href="#work" @click="menuOpen = false">Work</a>
        <a href="#apps" @click="menuOpen = false">Apps</a>
        <a href="#about" @click="menuOpen = false">About</a>
        <a href="#experience" @click="menuOpen = false">Experience</a>
        <a href="#capabilities" @click="menuOpen = false">Capabilities</a>
      </nav>
      <a class="header-cta" href="mailto:oladimejigideon22@gmail.com">Let’s talk <span>↗</span></a>
      <button class="menu-button" aria-label="Toggle menu" @click="menuOpen = !menuOpen">
        <span></span><span></span>
      </button>
    </header>

    <main>
      <section id="top" class="hero">
        <div class="hero-kicker reveal">Full-stack developer · Mobile builder</div>
        <h1>
          I build digital products
          <span class="hero-line"><em>that work</em> in the real world.</span>
        </h1>
        <div class="hero-bottom">
          <p>I’m Oladimeji Gideon. With 5+ years in frontend development, I turn product ideas into dependable web platforms and mobile apps from interface to API.</p>
          <a class="circle-link" href="#work" aria-label="See selected work">
            <span>See my work</span>
            <b>↓</b>
          </a>
        </div>
        <div class="hero-stamp" aria-hidden="true">
          <svg viewBox="0 0 160 160">
            <defs><path id="textPath" d="M80,80 m-58,0 a58,58 0 1,1 116,0 a58,58 0 1,1 -116,0"/></defs>
            <text><textPath href="#textPath">DESIGN • DEVELOP • DELIVER • </textPath></text>
          </svg>
          <span>✦</span>
        </div>
      </section>

      <section id="work" class="work section-pad">
        <div class="section-heading">
          <div>
            <span class="eyebrow">Selected work</span>
            <h2>Projects with a purpose.</h2>
          </div>
          <p>A selection of interfaces and platforms I’ve helped bring from idea to working product.</p>
        </div>

        <div class="project-grid">
          <a v-for="project in projects" :key="project.name" class="project-card" :class="project.tone" :href="project.url" target="_blank" rel="noreferrer">
            <div class="project-meta">
              <span>{{ project.number }} / {{ project.type }}</span>
              <span class="arrow">↗</span>
            </div>
            <div class="project-copy">
              <h3>{{ project.name }}</h3>
              <p>{{ project.blurb }}</p>
              <div class="tags"><span v-for="tag in project.tags" :key="tag">{{ tag }}</span></div>
            </div>
            <div class="project-visual">
              <img :src="project.image" :alt="`${project.name} project screenshot`" loading="lazy" />
            </div>
          </a>
        </div>
        <details class="project-archive">
          <summary>
            <span><b>More projects</b><small>Explore the rest of my selected portfolio</small></span>
            <i aria-hidden="true">+</i>
          </summary>
          <div class="archive-grid">
            <component
              :is="project.url ? 'a' : 'article'"
              v-for="project in archiveProjects"
              :key="project.name"
              :href="project.url || undefined"
              :target="project.url ? '_blank' : undefined"
              :rel="project.url ? 'noreferrer' : undefined"
            >
              <div class="archive-image"><img :src="project.image" :alt="`${project.name} project screenshot`" loading="lazy" /></div>
              <div class="archive-title">
                <span><small>{{ project.type }}</small><strong>{{ project.name }}</strong></span>
                <b v-if="project.url">↗</b>
              </div>
              <p>{{ project.description }}</p>
            </component>
          </div>
        </details>
      </section>

      <section id="apps" class="apps section-pad">
        <div class="section-heading light">
          <div>
            <span class="eyebrow">Mobile products</span>
            <h2>Ideas that live<br />in your pocket.</h2>
          </div>
          <p>Cross-platform product experiences built around real customer journeys—from discovery and booking to vendor operations.</p>
        </div>

        <div class="app-showcase">
          <article class="app-card app-card-moed">
            <div class="app-copy">
              <span class="app-number">APP / 01</span>
              <h3>Moed</h3>
              <p>An event management and discovery system that helps people find experiences, book tickets, manage a wallet, and connect with event vendors.</p>
              <div class="tags"><span>React Native</span><span>Events</span><span>Marketplace</span></div>
            </div>
            <div class="phone-stage single">
              <img :src="moedImage" alt="Moed event management mobile app home screen" loading="lazy" />
            </div>
          </article>

          <article class="app-card app-card-bookamia">
            <div class="app-copy">
              <span class="app-number">APP / 02</span>
              <h3>Bookamia</h3>
              <p>A multi-booking marketplace for hotels, eateries, events, cabs and movies—with a dedicated vendor dashboard for listings, bookings, earnings and withdrawals.</p>
              <div class="tags"><span>React Native</span><span>Multi-booking</span><span>Vendor dashboard</span></div>
            </div>
            <div class="phone-stage trio">
              <img :src="bookamiaSplashImage" alt="Bookamia mobile app welcome screen" loading="lazy" />
              <img :src="bookamiaImage" alt="Bookamia multi-booking customer experience" loading="lazy" />
              <img :src="vendorDashboardImage" alt="Bookamia vendor dashboard showing listings and earnings" loading="lazy" />
            </div>
          </article>

          <article class="app-card app-card-biztidy">
            <div class="app-copy">
              <span class="app-number">APP / 03</span>
              <h3>BizTidy</h3>
              <p>A cleaning-services booking app for discovering residential, commercial and industrial services and managing appointments.</p>
              <div class="tags"><span>React Native</span><span>Services</span><span>Booking</span></div>
            </div>
            <div class="phone-stage single">
              <img :src="bizTidyImage" alt="BizTidy cleaning services booking mobile app" loading="lazy" />
            </div>
          </article>
        </div>
      </section>

      <section id="about" class="about section-pad">
        <div class="portrait-wrap">
          <div class="portrait-frame"><img :src="portrait" alt="Oladimeji Gideon" loading="lazy" /></div>
          <span class="location">Based in Lagos<br />Working worldwide</span>
        </div>
        <div class="about-copy">
          <span class="eyebrow">The person behind the pixels</span>
          <h2>Engineer by training.<br /><em>Builder by nature.</em></h2>
          <p class="large">I bridge the gap between a good idea and a product people can actually use—and help other developers learn to do the same.</p>
          <div class="about-columns">
            <p>My background in electrical and electronics engineering shaped how I solve problems: understand the system, remove the noise, and build for reliability.</p>
            <p>Today, I work across the stack  crafting Vue and Nuxt interfaces, Laravel and Livewire backends, and React Native apps with a strong eye for the product experience.</p>
          </div>
          <div class="signature">Oladimeji Gideon</div>
        </div>
      </section>

      <section id="experience" class="experience section-pad">
        <div class="section-heading">
          <div>
            <span class="eyebrow">Experience & education</span>
            <h2>Built through practice.<br /><em>Grounded in engineering.</em></h2>
          </div>
          <p>I’ve worked on client products, taught practical frontend development, and built a technical foundation through electrical and electronics engineering.</p>
        </div>
        <div class="experience-grid">
          <div class="timeline">
            <article v-for="item in experience" :key="item.company">
              <span class="period">{{ item.period }}</span>
              <div>
                <h3>{{ item.role }}</h3>
                <p class="company">{{ item.company }} · {{ item.location }}</p>
                <p>{{ item.summary }}</p>
              </div>
            </article>
          </div>
          <aside class="education-card">
            <span class="eyebrow">Education</span>
            <div>
              <small>2021 — 2022</small>
              <h3>Higher National Diploma</h3>
              <p>Electrical & Electronics Engineering, Power Option</p>
            </div>
            <div>
              <small>2017 — 2019</small>
              <h3>National Diploma</h3>
              <p>Electrical & Electronics Engineering</p>
            </div>
            <div>
              <small>2023 — 2024</small>
              <h3>National Youth Service Corps</h3>
              <p>Completed national service</p>
            </div>
          </aside>
        </div>
      </section>

      <section id="capabilities" class="capabilities section-pad">
        <div class="section-heading light">
          <div><span class="eyebrow">What I bring</span><h2>One builder.<br />The full picture.</h2></div>
          <p>I can move between product thinking, polished interfaces, backend logic and the mobile experience.</p>
        </div>
        <div class="capability-list">
          <article v-for="item in capabilities" :key="item.mark">
            <span>{{ item.mark }}</span><h3>{{ item.title }}</h3><p>{{ item.text }}</p><b>↗</b>
          </article>
        </div>
        <div class="stack-strip">
          <span v-for="item in stack" :key="item">{{ item }}</span>
        </div>
      </section>

      <section class="contact section-pad">
        <span class="eyebrow">Have a product in mind?</span>
        <h2>Let’s make something<br /><em>worth using.</em></h2>
        <a class="email-link" href="mailto:oladimejigideon22@gmail.com">oladimejigideon22@gmail.com <span>↗</span></a>
        <div class="contact-foot">
          <p>Available for full-time roles, select freelance projects and product collaborations.</p>
          <div>
            <a href="https://github.com/oladimeji221" target="_blank" rel="noreferrer">GitHub ↗</a>
            <a href="https://www.linkedin.com/in/gideon-oladimeji-41086a299/" target="_blank" rel="noreferrer">LinkedIn ↗</a>
            <a href="https://x.com/gideon_bethel" target="_blank" rel="noreferrer">X ↗</a>
          </div>
        </div>
      </section>
    </main>

    <footer><span>© {{ new Date().getFullYear() }} Oladimeji Gideon</span><a href="#top">Back to top ↑</a></footer>
  </div>
</template>
