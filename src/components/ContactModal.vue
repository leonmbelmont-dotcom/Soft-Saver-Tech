<script setup>
defineProps({
  show: Boolean,
})
defineEmits(['close'])
</script>

<template>
  <div v-if="show" class="contact-modal" @click.self="$emit('close')">
    <div class="modal-content">
      <h3>Contacto</h3>
      <p>Elige tu forma preferida de contactarme:</p>
      <a href="mailto:leonmbelmont@gmail.com" class="modal-btn gmail-btn" @click="$emit('close')">
        📧 Gmail
      </a>
      <a
        href="https://github.com/leonmbelmont-dotcom"
        target="_blank"
        rel="noopener noreferrer"
        class="modal-btn github-btn"
        @click="$emit('close')"
      >
        🐙 GitHub
      </a>
      <a
        href="https://wa.me/5354753092"
        target="_blank"
        rel="noopener noreferrer"
        class="modal-btn whatsapp-btn"
        @click="$emit('close')"
      >
        💬 WhatsApp
      </a>
      <a
        href="https://www.instagram.com/soldier1stc/"
        target="_blank"
        rel="noopener noreferrer"
        class="modal-btn instagram-btn"
        @click="$emit('close')"
      >
        📸 Instagram
      </a>
      <button class="modal-btn close-btn" @click="$emit('close')">Cerrar</button>
    </div>
  </div>
</template>

<style scoped>
.contact-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
  animation: fadeIn 0.3s ease;
}

.modal-content {
  background: linear-gradient(90deg, #1e40af, #007acc);
  backdrop-filter: blur(10px);
  padding: 30px;
  border-radius: 15px;
  text-align: center;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.35);
  min-width: 300px;
  animation: slideUp 0.3s ease;
  border: 1px solid rgba(255, 255, 255, 0.12);
}

.modal-content h3 {
  margin-bottom: 15px;
  color: white;
  font-size: 20px;
  font-weight: bold;
}

.modal-content p {
  color: rgba(255, 255, 255, 0.9);
  margin-bottom: 20px;
  font-size: 14px;
}

.modal-btn {
  display: block;
  width: 100%;
  padding: 12px 20px;
  margin: 10px 0;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 16px;
  font-weight: bold;
  transition: all 0.3s ease;
  text-decoration: none;
  background: white;
  color: #007acc;
}

.modal-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.gmail-btn {
  background: #ea4335;
  color: white;
}

.gmail-btn:hover {
  background: #d33d2b;
}

.github-btn {
  background: #333333;
  color: white;
}

.github-btn:hover {
  background: #1a1a1a;
}

.whatsapp-btn {
  background: #25d366;
  color: white;
}

.whatsapp-btn:hover {
  background: #1fa85a;
}

.instagram-btn {
  background: #e1306c;
  color: white;
}

.instagram-btn:hover {
  background: #c91854;
}

.close-btn {
  background: rgba(255, 255, 255, 0.2);
  color: white;
  border: 1px solid rgba(255, 255, 255, 0.3);
  margin-top: 20px;
}

.close-btn:hover {
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

@keyframes slideUp {
  from {
    transform: translateY(50px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}
</style>
