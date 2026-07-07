<script setup lang="ts"></script>

<template>
  <div class="container">
    <section class="hero">
      <h1 class="hero-title">Vance Perry</h1>
      <p class="hero-desc">
        I am a high school senior and self-taught developer with 6+ years of programming experience.
      </p>
      <p class="hero-desc">I am good with web development, low-level systems, and networking.</p>
      <p class="hero-stack">
        Go &middot; Python &middot; C / C++ &middot; JavaScript / HTML / CSS &middot; Assembly
      </p>
      <div class="hero-links">
        <a href="#/projects" class="hero-link">projects &rarr;</a>
        <a href="#/contact" class="hero-link">contact &rarr;</a>
      </div>
    </section>
  </div>
</template>

<style scoped>
.hero {
  max-width: 600px;
}

.hero-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 24px;
  letter-spacing: -0.02em;
}

.hero-desc {
  color: var(--text-dim);
  margin-bottom: 16px;
  font-size: 0.95rem;
}

.hero-stack {
  color: var(--accent);
  font-size: 0.88rem;
  margin-bottom: 16px;
  line-height: 1.8;
}

.hero-links {
  display: flex;
  gap: 24px;
  margin-top: 32px;
}

.hero-link {
  color: var(--accent);
  font-size: 0.95rem;
}
</style>
