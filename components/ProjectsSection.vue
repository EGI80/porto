<template>
  <section class="projects" id="project">
    <div class="container">
      <h2>My Projects</h2>
      <div class="project-list">
        <div 
          class="project-card"
          v-for="project in projects"
          :key="project.id"
          @mouseover="onMouseOver(project.id)"
          @mouseleave="onMouseLeave"
          :style="{ transform: isActive(project.id) ? 'scale(1.1)' : 'scale(1)' }"
        >
          <img :src="project.image" :alt="project.title" class="project-image"/>
          <div class="project-content">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <a :href="project.link" class="project-link" target="_blank">Learn More</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ProjectsSection',
  data() {
    return {
      projects: [
        { 
          id: 1, 
          title: 'Project One', 
          description: 'Description for project one.', 
          image: 'https://via.placeholder.com/150', 
          link: 'https://example.com/project-one' 
        },
        { 
          id: 2, 
          title: 'Project Two', 
          description: 'Description for project two.', 
          image: 'https://bootdey.com/img/Content/avatar/avatar7.png', 
          link: 'https://example.com/project-two' 
        },
        
      ],
      activeProjectId: null
    }
  },
  methods: {
    onMouseOver(projectId) {
      this.activeProjectId = projectId;
    },
    onMouseLeave() {
      this.activeProjectId = null;
    },
    isActive(projectId) {
      return this.activeProjectId === projectId;
    }
  }
}
</script>

<style scoped>
.projects {
  padding: 50px 0;
  background-color: #0C1844;
  border-bottom: 2px solid #dc3545;
  
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

h2 {
  text-align: center;
  margin-bottom: 40px;
  font-size: 2.5em;
  color: #00FFEE;
  text-shadow: 0 0 10px #00FFEE, 0 0 20px #00FFEE;
}

.project-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.project-card {
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  max-width: 300px;
  text-align: center;
  transition: transform 0.3s ease;
  background:  rgba(0, 0, 100, 0.9);
}

.project-image {
  width: 100%;
  height: auto;
  transition: transform 0.3s ease;
}

.project-content {
  padding: 20px;
}

.project-content h3 {
  margin-bottom: 10px;
  font-size: 1.5em;
  color: #ffffff;
}

.project-content p {
  margin-bottom: 20px;
  color: #ffffff;
}

.project-link {
  display: inline-block;
  padding: 10px 20px;
  background: #007bff;
  color: #fff;
  text-decoration: none;
  border-radius: 4px;
  transition: background 0.3s;
}

.project-link:hover {
  background: #0056b3;
}
</style>
