<script setup>
import skill1 from '@/assets/images/skill1.png'
import skill2 from '@/assets/images/skill2.png'
import skill3 from '@/assets/images/skill3.png'
import skill4 from '@/assets/images/skill4.png'
import skill5 from '@/assets/images/skill5.png'
</script>

<template>
  <div class="container">
    <section class="about" id="sobre-mi">
      <h2>Sobre mí</h2>
      <p class="justified">
        Soy Leonardo ("Leonxsoldier"), desarrollador frontend con interés en interfaces limpias y
        accesibles. Me especializo en HTML, CSS moderno, JavaScript y actualmente trabajo en la
        incorporacion de frameworks como VUE.
      </p>

      <h3>Habilidades</h3>
      <ul class="skills">
        <li>
          <img :src="skill1" alt="HTML5" class="skill-icon" />
          <span>HTML5</span>
        </li>
        <li>
          <img :src="skill2" alt="CSS3" class="skill-icon" />
          <span>CSS3 (Grid / Flexbox)</span>
        </li>
        <li>
          <img :src="skill3" alt="JavaScript" class="skill-icon" />
          <span>JavaScript (Vanilla)</span>
        </li>
        <li>
          <img :src="skill4" alt="Vue" class="skill-icon" />
          <span>VUE (Framework)</span>
        </li>
        <li>
          <img :src="skill5" alt="Accesibilidad" class="skill-icon" />
          <span>Accesibilidad (Multiplataforma)</span>
        </li>
      </ul>

      <h3>Experiencia</h3>
      <p class="justified">
        He trabajado en proyectos escolares y personales creando landing pages, pequeñas apps y
        componentes reutilizables.
      </p>

      <div class="features">
        <span class="feature">✅ Diseño Responsivo</span>
        <span class="feature">✅ Optimizado SEO</span>
        <span class="feature">✅ Rendimiento Rápido</span>
        <span class="feature">✅ Código Limpio</span>
      </div>
    </section>
  </div>
</template>

<style scoped>
.skills {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1rem;
  list-style: none;
  padding: 0;
  margin: 1rem 0 2rem;
}

.skills li {
  display: flex;
  align-items: center;
  gap: 0.85rem;
  padding: 1rem 1rem;
  border-radius: 1rem;
  background: rgba(255, 255, 255, 0.08);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 12px 25px rgba(15, 23, 42, 0.08);
  color: #f8fafc;
  font-weight: 600;
}

.skill-icon {
  width: 42px;
  height: 42px;
  border-radius: 12px;
  object-fit: contain;
  border: 1px solid rgba(255, 255, 255, 0.14);
  background: rgba(255, 255, 255, 0.05);
  padding: 6px;
}
</style>
