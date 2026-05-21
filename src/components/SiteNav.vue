<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import AvatarModal from './AvatarModal.vue'
import ContactModal from './ContactModal.vue'

const menuOpen = ref(false)
const avatarModalOpen = ref(false)
const contactModalOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}

const openAvatarModal = (e) => {
  e.preventDefault()
  avatarModalOpen.value = true
}

const openContactModal = (e) => {
  e.preventDefault()
  contactModalOpen.value = true
}

const closeAvatarModal = () => {
  avatarModalOpen.value = false
}

const closeContactModal = () => {
  contactModalOpen.value = false
}
</script>

<template>
  <nav class="navbar">
    <div class="nav-container">
      <a href="#" class="nav-logo" @click="openAvatarModal">
        <img src="@/assets/images/profile.jpg" alt="Leonxsoldier" class="logo-img" />
        <div class="nav-user-info">
          <span class="nav-user-name">Leonxsoldier</span>
          <span class="nav-user-email">leonmbelmont@gmail.com</span>
        </div>
      </a>

      <div class="hamburger" :class="{ active: menuOpen }" @click="toggleMenu" aria-label="Menú">
        <span></span>
        <span></span>
        <span></span>
      </div>

      <ul class="nav-menu" :class="{ active: menuOpen }">
        <li><RouterLink to="/" class="nav-link" @click="closeMenu">Inicio</RouterLink></li>
        <li>
          <RouterLink to="/services" class="nav-link" @click="closeMenu">Servicios</RouterLink>
        </li>
        <li><RouterLink to="/about" class="nav-link" @click="closeMenu">Sobre Mí</RouterLink></li>
        <li>
          <RouterLink to="/portfolio" class="nav-link" @click="closeMenu">Portafolio</RouterLink>
        </li>
        <li>
          <a href="#" class="nav-link nav-link-btn" @click="openContactModal">Contacto</a>
        </li>
      </ul>
    </div>
  </nav>

  <AvatarModal :show="avatarModalOpen" @close="closeAvatarModal" />
  <ContactModal :show="contactModalOpen" @close="closeContactModal" />
</template>
