<script setup lang="ts">
const links = [
  {
    label: 'email',
    href: 'mailto:admin@killallchickens.org',
    desc: 'admin@killallchickens.org',
  },
  {
    label: 'discord',
    href: 'https://discord.com/users/830519520031670303',
    desc: '@epicman121',
  },
  {
    label: 'github',
    href: 'https://github.com/KillAllChickens',
    desc: 'KillAllChickens',
  },
]
</script>

<template>
  <div class="container">
    <h1 class="page-title">contact</h1>
    <p class="page-desc">Ways to reach me.</p>
    <div class="links">
      <a
        v-for="link in links"
        :key="link.label"
        :href="link.href"
        target="_blank"
        rel="noopener"
        class="link-card"
      >
        <span class="link-label">{{ link.label }}</span>
        <span class="link-desc">{{ link.desc }}</span>
        <span class="link-arrow">&#x2197;</span>
      </a>
    </div>
  </div>
</template>

<style scoped>
.page-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 8px;
  letter-spacing: -0.02em;
}

.page-desc {
  color: var(--text-dim);
  margin-bottom: 32px;
  font-size: 0.95rem;
}

.links {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.link-card {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 16px 20px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  color: var(--text);
  font-size: 0.9rem;
  transition: border-color 0.15s;
}

.link-card:hover {
  border-color: var(--border-light);
  text-decoration: none;
}

.link-label {
  color: var(--accent);
  font-weight: 500;
  min-width: 70px;
}

.link-desc {
  color: var(--text-dim);
  flex: 1;
}

.link-arrow {
  color: var(--text-muted);
  font-size: 1rem;
}
</style>
