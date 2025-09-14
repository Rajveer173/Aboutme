

<template>
  <div class="portfolio-bg">
    <section class="intro">
      <h1>Rajveer K P</h1>
      <p class="subtitle">Software Engineer | Cloud Enthusiast | Solution Architect</p>
      <p class="desc">Building robust solutions with code, design, and innovation.</p>
    </section>

    <section class="skills">
      <h2>Skills</h2>
      <div class="skills-list">
        <div class="skill-category">
          <h3>Programming Languages</h3>
          <SkillBar name="Python" color="#3572A5" />
          <SkillBar name="Java" color="#b07219" />
          <SkillBar name="C#" color="#178600" />
          <SkillBar name="C" color="#555555" />
          <SkillBar name="SQL" color="#e38c00" />
          <SkillBar name="Kotlin" color="#7f52ff" />
          <SkillBar name="JavaScript" color="#f7df1e" />
        </div>
        <div class="skill-category">
          <h3>Frameworks & Technologies</h3>
          <SkillBar name="Django" color="#092e20" />
          <SkillBar name="Vue.js" color="#42b883" />
          <SkillBar name="React" color="#61dafb" />
          <SkillBar name="Node.js" color="#3c873a" />
          <SkillBar name="Spring Boot" color="#6db33f" />
        </div>
        <div class="skill-category">
          <h3>Other</h3>
          <ul class="other-skills">
            <li>Cloud Engineering Basics</li>
            <li>AWS</li>
            <li>Azure</li>
            <li>System Commands</li>
            <li>Software Infrastructure</li>
            <li>Solution Architecture</li>
            <li>UML/ML Techniques</li>
            <li>Data Modeling</li>
            <li>Wireframing & Prototyping</li>
            <li>Documentation</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="linux-hands-on">
      <h2>Hands-on Linux for ML / UML Testing</h2>
      <div class="linux-training">
        <ul>
          <li>Setting up Python virtual environments for ML experiments</li>
          <li>Automating data preprocessing and model training with Bash scripts</li>
          <li>Running JupyterLab and managing kernels on remote Linux servers</li>
          <li>Batch evaluation and testing of ML models using shell pipelines</li>
          <li>Using UML tools (PlantUML, yEd) via Linux CLI for architecture diagrams</li>
          <li>Automated test execution and reporting with pytest and shell integration</li>
          <li>Monitoring GPU/CPU usage for ML workloads (nvidia-smi, htop)</li>
          <li>Versioning and tracking experiments with Git and DVC on Linux</li>
        </ul>
      </div>
    </section>

    <section class="projects">
      <h2>Projects</h2>
      <div class="project-cards">
        <ProjectCard
          title="Quiz Master"
          link="https://github.com/Rajveer-kp/quiz_master_23f3000717.git"
          description="A full-featured quiz platform with robust backend and interactive UI."
        />
        <ProjectCard
          title="Vehicle Parking App"
          link="https://github.com/Rajveer-kp/_Vehicle_Parking_App_23f3000717.-.git"
          description="Smart parking management system with real-time tracking and analytics."
        />
      </div>
    </section>

    <footer>
      <p>© 2025 Rajveer K P &mdash; Crafted with Vue.js ⚡</p>
    </footer>
  </div>
</template>

<script setup>
import SkillBar from './components/SkillBar.vue'
import ProjectCard from './components/ProjectCard.vue'
</script>

<style scoped>
.portfolio-bg {
  min-height: 100vh;
  width: 100%;
  max-width: 100vw;
  background: linear-gradient(135deg, #232526 0%, #414345 100%);
  color: #fff;
  font-family: 'Segoe UI', 'Roboto', Arial, sans-serif;
  padding-bottom: 40px;
  animation: bgfade 2s;
  overflow-x: auto;
  margin: 0 auto;
  box-sizing: border-box;
}
.linux-commands {
  margin: 48px auto 0 auto;
  max-width: 900px;
  background: rgba(30,40,60,0.7);
  border-radius: 18px;
  padding: 32px 24px;
  box-shadow: 0 4px 32px #0002;
  .skills, .projects, .linux-hands-on {
    margin: 40px auto 0 auto;
    max-width: 680px;
    background: rgba(30,40,60,0.7);
    border-radius: 18px;
    padding: 28px 16px;
    box-shadow: 0 4px 32px #0002;
    animation: fadein 1.2s;
  }
  .projects {
    margin: 48px auto 0 auto;
    animation: fadein 1.6s;
  }
  .linux-hands-on {
    margin: 48px auto 0 auto;
    animation: fadein 1.8s;
  }
  .linux-training ul {
    list-style: disc inside;
    color: #b0eaff;
    font-size: 1.08rem;
    padding-left: 1.2em;
    margin: 0;
  }
  .linux-training li {
    margin-bottom: 10px;
    line-height: 1.6;
    font-weight: 500;
    letter-spacing: 0.1px;
  }
}
.skills {
  margin: 40px auto 0 auto;
  max-width: 900px;
  background: rgba(30,40,60,0.7);
  border-radius: 18px;
  padding: 32px 24px;
  box-shadow: 0 4px 32px #0002;
  animation: fadein 1.2s;
}
.skills-list {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
  justify-content: space-between;
}
.skill-category {
  flex: 1 1 250px;
  min-width: 220px;
}
.skill-category h3 {
  margin-bottom: 10px;
  color: #42b883;
}
.other-skills {
  list-style: none;
  padding: 0;
  color: #f7df1e;
  font-size: 1rem;
}
.projects {
  margin: 48px auto 0 auto;
  max-width: 900px;
  background: rgba(30,40,60,0.7);
  border-radius: 18px;
  padding: 32px 24px;
  box-shadow: 0 4px 32px #0002;
  animation: fadein 1.6s;
}
.project-cards {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
  justify-content: center;
}
footer {
  text-align: center;
  margin-top: 60px;
  color: #b0eaff;
  font-size: 1rem;
  opacity: 0.7;
}
@keyframes fadein {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: none; }
}
@media (max-width: 900px) {
  .skills, .projects, .linux-hands-on {
    max-width: 98vw;
    margin-left: 1vw;
    margin-right: 1vw;
    padding: 18px 6px;
  }
  .skills-list, .project-cards {
    flex-direction: column;
    gap: 18px;
  }
}
</style>
