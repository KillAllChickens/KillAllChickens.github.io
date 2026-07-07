<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="layout">
    <nav class="nav">
      <div class="container nav-inner">
        <router-link to="/" class="nav-logo">Vance Perry</router-link>
        <div class="nav-links">
          <router-link to="/" class="nav-link" exact>home</router-link>
          <router-link to="/projects" class="nav-link">projects</router-link>
          <router-link to="/contact" class="nav-link">contact</router-link>
        </div>
      </div>
    </nav>

    <main class="main">
      <RouterView />
    </main>

    <footer class="footer">
      <div class="container">
        <p>
          No rights reserved, this is all MIT:
          <a href="https://github.com/KillAllChickens/KillAllChickens.github.io" target="_blank"
            >feel free to take the code on Github</a
          >
        </p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.nav {
  border-bottom: 1px solid var(--border);
  background: var(--bg);
  position: sticky;
  top: 0;
  z-index: 10;
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 56px;
}

.nav-logo {
  font-weight: 700;
  color: var(--text);
  font-size: 1rem;
}

.nav-logo:hover {
  text-decoration: none;
  color: var(--accent);
}

.nav-links {
  display: flex;
  gap: 4px;
}

.nav-link {
  padding: 6px 12px;
  border-radius: 6px;
  font-size: 0.85rem;
  color: var(--text-dim);
}

.nav-link:hover {
  color: var(--text);
  background: var(--accent-muted);
  text-decoration: none;
}

.nav-link.router-link-exact-active {
  color: var(--accent);
}

.main {
  padding: 80px 0;
  min-height: calc(100vh - 112px);
}

.footer {
  border-top: 1px solid var(--border);
  padding: 24px 0;
  color: var(--text-muted);
  font-size: 0.8rem;
}
</style>
