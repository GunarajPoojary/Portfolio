<template>
  <div style="margin-bottom: 80px;">
    <h1 class="cascade" style="--delay: 0ms">Hello!</h1>

    <div class="paragraph">
      <div class="cascade" style="--delay: 100ms">
        I'm <strong>Gunaraj Poojary</strong>, a passionate Unity game developer with 
        <span class="highlight">6 months</span> of hands-on experience in <span class="highlight">Game Development</span>.
  <br /><br />
  I specialize in designing and building clean, scalable, and optimized C# code using industry-standard best practices.
  <br /><br />
        My expertise includes:
        <span class="highlight">Object-Oriented Programming (OOP)</span>,
        <span class="highlight">Design Patterns</span>,
        <span class="highlight">SOLID Principles</span>,
        <span class="highlight">Editor Scripting</span>,
        <span class="highlight">API integration</span>, and more.
        <br /><br />
        I've worked on various <router-link to="/game-projects">Projects</router-link>, including 2D/3D games and applications, and I'm always eager to learn and explore new technologies.
        <br /><br />
        I am currently seeking opportunities to work on exciting projects that challenge my skills and allow me to grow as a developer.
        <br /><br />
        If you're looking for a dedicated and enthusiastic game developer, feel free to <router-link to="/contact">contact me</router-link>.
        <br /><br />
      </div>
    </div>

    <span class="photo">
        <img src="img/avatar.png" alt="Avatar of Gunaraj" />
      </span>

    <div style="clear: both;"></div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "About",
  mounted() {
    window.scrollTo(0, 0);
  }
});
</script>

<style scoped>
.paragraph {
  max-width: 700px;
  margin-bottom: 20px;
}

.photo {
  float: right; /* or right */
  padding-left: 40px;
}

.photo img {
  max-width: 350px;
  width: 100%;
  height: auto;
  border-radius: 12px;
}

@media only screen and (min-width: 620px) {
  .paragraph {
    float: left;
  }

  .photo {
  float: none;
  margin: 20px auto;
  text-align: center;
  }
}

.highlight {
  background-color: #ff8000c9; /* warm glowing badge look */
  border-radius: 6px;
  padding: 2px 6px;
  font-weight: bold;
}

/* Fix for cascade animation */
.cascade {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeUp 0.5s forwards;
  animation-delay: var(--delay);
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>