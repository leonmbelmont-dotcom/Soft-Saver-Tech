<script setup>
import { ref } from 'vue'
import ContactModal from '@/components/ContactModal.vue'

const contactModalOpen = ref(false)

const openContactModal = (e) => {
  e.preventDefault()
  contactModalOpen.value = true
}

const closeContactModal = () => {
  contactModalOpen.value = false
}
</script>

<template>
  <div class="container">
    <section class="about" id="inicio">
      <h2>BIENVENIDO A SOFT SAVER TECH</h2>
      <p class="justified">
        Soft Saver Tech es una plataforma web diseñada para facilitar el soporte técnico de software
        informático. Aquí encontrarás atención rápida, soluciones confiables y una experiencia
        amigable que conecta usuarios con expertos. Navega por nuestros servicios, conoce el
        proyecto y descubre ejemplos de trabajo preparados especialmente para las necesidades
        digitales de cada cliente. Es una plataforma web diseñada para brindar soporte técnico
        relacionado con software informático. El objetivo principal es ofrecer un espacio accesible
        donde los clientes puedan plantear sus problemas y recibir soluciones rápidas y confiables.
        La plataforma busca combinar un diseño moderno con una experiencia de usuario clara y
        sencilla, facilitando la interacción entre usuarios y especialistas. Además, pretende
        convertirse en un recurso integral para optimizar el uso de herramientas digitales, mejorar
        la productividad y garantizar la seguridad de los sistemas de los clientes.
      </p>
      <div class="features">
        <span class="feature">Servicios personalizados</span>
        <span class="feature">Resolución de errores</span>
        <span class="feature">Asesoría de software</span>
        <span class="feature">Seguridad y productividad</span>
      </div>
    </section>

    <section class="cta" id="contacto">
      <h2>¿Interesado en trabajar juntos?</h2>
      <p>Cuéntame sobre tu proyecto y cómo puedo ayudarte</p>
      <a class="hero-btn" href="#" @click="openContactModal">Contáctame Ahora</a>
    </section>
  </div>

  <ContactModal :show="contactModalOpen" @close="closeContactModal" />
</template>
