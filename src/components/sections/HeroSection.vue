<template>
    <section id="hero">
        <div class="hero-bg-glow g1"></div>
        <div class="hero-bg-glow g2"></div>
        <div class="hero-inner"
            style="
        max-width: 1100px;
        margin: 0 auto;
        width: 100%;
        position: relative;
        z-index: 1;
      ">
            <div class="hero-left">
                <div class="hero-tags">
                    <span class="hero-tag active">● Available for Work</span>
                    <span class="hero-tag">Full Stack</span>
                    <span class="hero-tag">Backend</span>
                </div>
                <div class="hero-name">
                    <div class="hero-name-line1">Muktashim</div>
                    <span class="hero-name-line2">Billah.</span>
                </div>
                <div class="hero-title-wrap">
                    <span class="hero-title-label">Building scalable backends, elegant APIs, and modern frameworks —
                        from</span>
                </div>
                <div class="hero-title-wrap" style="margin-bottom: 0.75rem">
                    <span class="hero-title-typed" id="typed-text"></span><span class="hero-title-cursor"></span>
                </div>
                <p class="hero-desc">
                    I'm a Full Stack Developer with a strong focus on backend engineering
                    — designing scalable APIs, clean MVC architectures and robust database
                    systems with Laravel and MySQL. I'm currently expanding my frontend
                    craft with React and Tailwind CSS to deliver complete, polished
                    products end-to-end.
                </p>
                <div class="hero-btns">
                    <a href="#projects" class="btn-primary">
                        <Icon name="arrow-right" size="13" />
                        View Projects
                    </a>
                    <a href="#" class="btn-outline">
                        <Icon name="download" size="13" />
                        Download CV
                    </a>
                    <a href="#contact" class="btn-outline">Let's Connect</a>
                </div>
                <div class="hero-stats">
                    <div>
                        <div class="hero-stat-num"><span id="c1">0</span>+</div>
                        <div class="hero-stat-label">Projects Completed</div>
                    </div>
                    <div>
                        <div class="hero-stat-num"><span id="c2">0</span>+</div>
                        <div class="hero-stat-label">Years of Experience</div>
                    </div>
                    <div>
                        <div class="hero-stat-num">
                            <span id="c3">3</span>.<span id="c4">0</span>
                        </div>
                        <div class="hero-stat-label">GPA / Academic Score</div>
                    </div>
                </div>
            </div>
            <div class="hero-right">
                <div class="hero-avatar-wrap">
                    <div class="hero-avatar-ring"></div>

                    <div class="hero-floating-badge b1">
                        <span class="b-dot" style="background: #f97316"></span>⚡ Laravel
                    </div>
                    <div class="hero-floating-badge b2">
                        <span class="b-dot" style="background: #3b82f6"></span>🔗 REST API
                    </div>
                    <div class="hero-floating-badge b3">
                        <span class="b-dot" style="background: #22c55e"></span>🟢 Available
                    </div>
                    <div class="hero-avatar">
                        <img src="../../assets/profile.jpg" alt="Muktashim Billah" class="hero-avatar-img" />
                    </div>
                </div>
                <div
                    style="
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
            min-width: 160px;
          ">
                    <div
                        style="
              background: var(--surface);
              border: 1px solid var(--border);
              border-radius: 8px;
              padding: 0.6rem 0.85rem;
              display: flex;
              align-items: center;
              gap: 0.5rem;
            ">
                        <span style="font-size: 0.75rem">⭐</span>
                        <span style="font-size: 0.7rem; color: var(--text2)">4+ Projects Built</span>
                    </div>
                    <div
                        style="
              background: var(--surface);
              border: 1px solid var(--border);
              border-radius: 8px;
              padding: 0.6rem 0.85rem;
              display: flex;
              align-items: center;
              gap: 0.5rem;
            ">
                        <span style="font-size: 0.75rem">🏔️</span>
                        <span style="font-size: 0.7rem; color: var(--text2)">Kerinci Ticketing Live</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="hero-scroll-hint"></div>
    </section>
</template>

<script>
    import Icon from "../ui/Icon.vue";

    export default {
        components: {
            Icon
        },
    };
</script>
