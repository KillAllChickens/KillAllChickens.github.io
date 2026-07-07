<script setup lang="ts">
import ProjectCard from '@/components/ProjectCard.vue'
import { projects } from '@/data/projects'
</script>

<template>
  <div class="container">
    <h1 class="page-title">projects</h1>
    <div class="grid">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :category="project.category"
        :tags="project.tags"
        :stack="project.stack ?? []"
        :description="project.description"
        :link="project.link"
      />
    </div>
  </div>
</template>

<style scoped>
.page-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 32px;
  letter-spacing: -0.02em;
}

.grid {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
</style>
