<template>
  <nav>
    <a href="#" class="nav-logo">
      <div class="nav-logo-dot"></div>
      Muktashim Billah.
    </a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#learning">Learning</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="nav-right">
      <a
        href="https://github.com/muktashimbillah"
        target="_blank"
        class="nav-icon-btn"
        title="GitHub">
        <Icon name="github" size="14" />
      </a>
      <a
        href="https://www.linkedin.com/in/muktashim-billah-6a1000222/"
        target="_blank"
        class="nav-icon-btn"
        title="LinkedIn">
        <Icon name="linkedin" size="14" />
      </a>
      <a href="mailto:muktashim@email.com" class="nav-hire">Hire Me</a>
    </div>
  </nav>
</template>

<script>
import Icon from "./Icon.vue";

export default {
  components: { Icon },
};
</script>
