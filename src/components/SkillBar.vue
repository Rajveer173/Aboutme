<template>
  <div class="skill-bar">
    <span class="skill-label">{{ name }}</span>
    <div class="bar-bg">
      <div class="bar-fill" :style="barStyle"></div>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
const props = defineProps({
  name: String,
  color: String
})
const barStyle = computed(() => ({
  width: '100%',
  background: `linear-gradient(90deg, ${props.color} 60%, #232526 100%)`,
  transition: 'width 1.2s cubic-bezier(.4,2,.6,1)',
  boxShadow: `0 0 8px ${props.color}88`
}))
</script>

<style scoped>
.skill-bar {
  display: flex;
  align-items: center;
  margin-bottom: 16px;
  gap: 16px;
}
.skill-label {
  min-width: 110px;
  font-weight: 600;
  color: #b0eaff;
  font-size: 1.08rem;
  letter-spacing: 0.5px;
}
.bar-bg {
  flex: 1;
  height: 14px;
  background: #222c3a;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 1px 6px #0002;
}
.bar-fill {
  height: 100%;
  border-radius: 8px;
  opacity: 0.92;
  animation: barGrow 1.2s cubic-bezier(.4,2,.6,1);
}
@keyframes barGrow {
  from { width: 0; }
  to { width: 100%; }
}
</style>
