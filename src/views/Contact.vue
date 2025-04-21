<template>
  <div>
    <h1 style="--delay: 0ms">Let's get in touch</h1>

    <div class="cascade" style="--delay: 100ms; margin-bottom:40px;">
      I'm looking for a job!. Feel free to contact me about any opportunity.
    </div>

    <ul>
        <i class="fa fa-envelope-o fa-lg fa-fw"></i>
        <a href="mailto:gunarajpoojary579@email.com" target="_blank">gunarajpoojary579@email.com</a>
      <br /><br />
        <i class="fa fa-linkedin fa-lg fa-fw" style="vertical-align: -5%;"></i>
        <a href="https://www.linkedin.com/in/gunarajpoojary" target="_blank">www.linkedin.com/in/gunarajpoojary</a>
      <br /><br />
        <i class="fa fa-github fa-lg fa-fw"></i>
        <a href="https://github.com/GunarajPoojary" target="_blank">https://github.com/GunarajPoojary</a>
      <br /><br />
        <i class="fa fa-gamepad fa-lg fa-fw"></i>
        <a href="https://gunarajpoojary.itch.io/" target="_blank">https://gunarajpoojary.itch.io/</a>
      <br /><br />
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Contact",
  mounted() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
});
</script>

<style scoped>
div {
  margin-bottom: 150px;
}

ul {
  list-style: none;
  padding-inline-start: 0px;
}

li {
  line-height: 1.8em;
  font-size: 1.2em;
}

@media only screen and (min-width: 620px){
  ul {
    padding-inline-start: 40px;
  }

  li {
    line-height: 2em;
    font-size: 1.4em;
  }
}

i {
  margin-right: 20px;
}

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