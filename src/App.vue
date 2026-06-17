<template>
  <div>
    <NavBar />
    <SideNav />
    <HeroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectsSection />
    <ExperienceSection />
    <LearningSection />
    <ContactSection @sendMsg="sendMsg" />
    <FooterSection />
  </div>
</template>

<script>
import "./styles/global.css";
import NavBar from "./components/NavBar.vue";
import SideNav from "./components/SideNav.vue";
import HeroSection from "./components/HeroSection.vue";
import AboutSection from "./components/AboutSection.vue";
import SkillsSection from "./components/SkillsSection.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import ExperienceSection from "./components/ExperienceSection.vue";
import LearningSection from "./components/LearningSection.vue";
import ContactSection from "./components/ContactSection.vue";
import FooterSection from "./components/FooterSection.vue";

export default {
  components: {
    NavBar,
    SideNav,
    HeroSection,
    AboutSection,
    SkillsSection,
    ProjectsSection,
    ExperienceSection,
    LearningSection,
    ContactSection,
    FooterSection,
  },
  mounted() {
    this.initTyping();
    this.initCounter();
    this.initReveal();
    this.initSideNav();
    this.initScrollNav();
  },
  methods: {
    initTyping() {
      const titles = [
        "Full Stack Developer",
        "Backend Engineer",
        "Laravel Developer",
        "API Developer",
      ];
      let ti = 0;
      let ci = 0;
      let del = false;
      const el = document.getElementById("typed-text");
      const type = () => {
        const w = titles[ti];
        if (!del) {
          el.textContent = w.slice(0, ++ci);
          if (ci === w.length) {
            del = true;
            setTimeout(type, 2000);
            return;
          }
        } else {
          el.textContent = w.slice(0, --ci);
          if (ci === 0) {
            del = false;
            ti = (ti + 1) % titles.length;
          }
        }
        setTimeout(type, del ? 55 : 85);
      };
      type();
    },
    initCounter() {
      const counter = (id, target) => {
        let n = 0;
        const s = Math.ceil(target / 40);
        const t = setInterval(() => {
          n = Math.min(n + s, target);
          document.getElementById(id).textContent = n;
          if (n >= target) clearInterval(t);
        }, 30);
      };
      const cObs = new IntersectionObserver(
        (entries, observer) => {
          if (entries[0].isIntersecting) {
            counter("c1", 18);
            counter("c2", 22);
            observer.disconnect();
          }
        },
        { threshold: 0.3 },
      );
      const hero = document.getElementById("hero");
      if (hero) cObs.observe(hero);
    },
    initReveal() {
      const revObs = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) entry.target.classList.add("visible");
          });
        },
        { threshold: 0.08 },
      );
      document.querySelectorAll(".reveal").forEach((el) => revObs.observe(el));
    },
    initSideNav() {
      const sections = [
        "hero",
        "about",
        "skills",
        "projects",
        "experience",
        "learning",
        "contact",
      ];
      const dots = document.querySelectorAll(".side-dot");
      dots.forEach((dot, i) => {
        dot.addEventListener("click", () => {
          const target = document.getElementById(sections[i]);
          if (target) target.scrollIntoView({ behavior: "smooth" });
        });
      });
      const secObs = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              const i = sections.indexOf(entry.target.id);
              dots.forEach((dot) => dot.classList.remove("active"));
              if (i >= 0) dots[i].classList.add("active");
            }
          });
        },
        { threshold: 0.3 },
      );
      sections.forEach((id) => {
        const el = document.getElementById(id);
        if (el) secObs.observe(el);
      });
    },
    initScrollNav() {
      window.addEventListener("scroll", () => {
        const borderColor =
          window.scrollY > 40
            ? "rgba(255,255,255,.08)"
            : "rgba(255,255,255,.04)";
        const nav = document.querySelector("nav");
        if (nav) nav.style.borderBottomColor = borderColor;
      });
    },
    sendMsg() {
      const form = document.getElementById("cform");
      const success = document.getElementById("fsuccess");
      if (form && success) {
        form.style.display = "none";
        success.style.display = "block";
        setTimeout(() => {
          form.style.display = "flex";
          success.style.display = "none";
          form.reset();
        }, 4000);
      }
    },
  },
};
</script>
