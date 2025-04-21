<template>
  <div class="projects-layout">
    <!-- Left Tabs -->
    <div class="tabs">
      <div
      v-for="project in projects"
      :key="project.id"
        :class="{ active: activeTab === project.id }"
        @click="scrollTo(project.id)"
      >
        {{ project.name }}
      </div>
    </div>

    <!-- Right Scrollable Project Content -->
    <div class="projects-scroll">
      <div
        v-for="project in projects"
        :key="project.id"
        :id="project.id"
        class="project-block"
      >
        <div class="project-info">
          <h2>{{ project.name }}</h2>
          <p>{{ project.description }}</p>
          <a :href="project.webgl" target="_blank" class="project-link">Play WebGL</a>
          <a :href="project.github" target="_blank" class="project-link">View GitHub</a>
        </div>
        <div class="project-video">
          <iframe
            :src="project.videoUrl"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import gameProjectsData from "@/data/GameProjectsData";

export default Vue.extend({
  name: "GameProjects",
  data() {
    return {
      projects: gameProjectsData,
      activeTab: ""
    };
  },
  mounted() {
    this.activeTab = this.projects[0]?.id || "";
    window.scrollTo({ top: 0, behavior: 'smooth' });
  },
  methods: {
    scrollTo(id: string) {
      this.activeTab = id;
      const target = document.getElementById(id);
      if (target) {
        target.scrollIntoView({ behavior: "smooth", block: "start" });
      }
    }
  }
});
</script>

<style scoped>
.projects-layout {
  display: flex;
  gap: 1rem;
  padding: 20px;
}

.tabs {
  position: sticky;
  top: 100px;
  height: fit-content;
  min-width: 180px;
  border-right: 1px solid #ccc;
}

.tabs div {
  padding: 12px 16px;
  cursor: pointer;
  font-weight: 500;
  border-left: 3px solid transparent;
  transition: background 0.2s, border-color 0.2s;
}

.tabs div:hover,
.tabs div.active {
  background-color: #f0f0f0;
  border-left: 3px solid #00F0FF;
}

.projects-scroll {
  flex: 1;
  overflow-y: auto;
  padding-left: 10px;
  max-height: 85vh;
  scroll-behavior: smooth;
}

.project-block {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  padding: 30px 0;
  border-bottom: 1px solid #ddd;
}

.project-info {
  flex: 1 1 300px;
}

.project-video {
  flex: 1 1 400px;
  min-width: 300px;
}

.project-video iframe {
  width: 100%;
  height: 225px;
  border-radius: 8px;
}

.project-link {
  display: inline-block;
  margin-top: 10px;
  margin-right: 15px;
  color: #00F0FF;
  text-decoration: underline;
}
</style>