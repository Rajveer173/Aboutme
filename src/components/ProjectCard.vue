<template>
  <div class="project-card" @mousemove="handleMove" @mouseleave="resetTilt" :style="tiltStyle">
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
    <a :href="link" target="_blank" class="project-link">View on GitHub →</a>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const props = defineProps({
  title: String,
  link: String,
  description: String
})
const tiltX = ref(0)
const tiltY = ref(0)
const tiltStyle = ref({})
function handleMove(e) {
  const card = e.currentTarget
  const rect = card.getBoundingClientRect()
  const x = e.clientX - rect.left
  const y = e.clientY - rect.top
  const centerX = rect.width / 2
  const centerY = rect.height / 2
  tiltX.value = (y - centerY) / 10
  tiltY.value = (x - centerX) / 10
  tiltStyle.value = {
    transform: `rotateX(${-tiltX.value}deg) rotateY(${tiltY.value}deg) scale(1.04)`
  }
}
function resetTilt() {
  tiltStyle.value = { transform: 'none' }
}
</script>

<style scoped>
.project-card {
  background: linear-gradient(120deg, #232526 60%, #42b883 120%);
  border-radius: 16px;
  box-shadow: 0 6px 32px #0004;
  padding: 28px 24px 22px 24px;
  min-width: 260px;
  max-width: 340px;
  color: #fff;
  transition: box-shadow 0.3s, transform 0.3s;
  cursor: pointer;
  margin-bottom: 8px;
  will-change: transform;
}
.project-card:hover {
  box-shadow: 0 12px 48px #42b88388, 0 2px 8px #0002;
}
.project-card h3 {
  margin: 0 0 10px 0;
  font-size: 1.3rem;
  color: #f7df1e;
}
.project-card p {
  font-size: 1rem;
  color: #e0e0e0;
  margin-bottom: 18px;
}
.project-link {
  color: #b0eaff;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: color 0.2s;
}
.project-link:hover {
  color: #f7df1e;
}
</style>
