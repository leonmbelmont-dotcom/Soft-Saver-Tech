<script setup>
defineProps({
  show: Boolean,
})
defineEmits(['close'])
</script>

<template>
  <div v-if="show" class="avatar-modal" @click.self="$emit('close')">
    <div class="avatar-content">
      <img src="@/assets/images/profile.jpg" alt="Leonardo Marcos" class="avatar-img-large" />
      <h3 class="avatar-name">Leonardo Marcos</h3>
      <p class="avatar-email">leonmbelmont@gmail.com</p>
      <button class="avatar-close" @click="$emit('close')">Cerrar</button>
    </div>
  </div>
</template>

<style scoped>
.avatar-modal {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1100;
  animation: fadeIn 0.2s ease;
}

.avatar-content {
  background: linear-gradient(90deg, #1e40af, #007acc);
  backdrop-filter: blur(8px);
  padding: 20px;
  border-radius: 12px;
  text-align: center;
  min-width: 280px;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.12);
}

.avatar-img-large {
  width: 320px;
  height: 320px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid rgba(255, 255, 255, 0.25);
  margin-bottom: 12px;
}

.avatar-name {
  color: white;
  font-weight: 800;
  margin-bottom: 4px;
}

.avatar-email {
  color: rgba(255, 255, 255, 0.9);
  font-size: 14px;
  margin-bottom: 12px;
}

.avatar-close {
  background: rgba(255, 255, 255, 0.2);
  color: white;
  padding: 8px 14px;
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.25);
  cursor: pointer;
  font-weight: 600;
  transition: all 0.3s ease;
}

.avatar-close:hover {
  background: rgba(255, 255, 255, 0.3);
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@media (max-width: 420px) {
  .avatar-img-large {
    width: 120px;
    height: 120px;
  }
}
</style>
