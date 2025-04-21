<template>
  <div>
    <h1 class="cascade" style="--delay: 0ms;">Resume</h1>

    <!-- Intro Section -->
    <div class="intro-container cascade" style="--delay: 100ms;">
      <div class="paragraph">
        I'm a passionate Unity Game Developer with hands-on experience in crafting interactive 2D and 3D applications. Based in Karnataka, India, I bring a strong technical foundation and a creative mindset to every project I work on.
        <br /><br />
        After graduating with a Bachelor's degree in Mechanical Engineering in 2022, I discovered my true calling in game development and have since dedicated myself to learning and building games that are both engaging and immersive.
        <br /><br />
        If you'd like to collaborate or learn more, feel free to <router-link to="/contact">contact me</router-link>.
        <br /><br />
        <div class="download-wrapper">
          <a class="download-link" href="/d/Resume(Gunaraj Poojary).pdf" download="Gunaraj_Resume.pdf">
            <i class="fa fa-download fa-lg fa-fw"></i> Download as PDF
          </a>
        </div>
      </div>

      <div class="resume-photo">
        <img src="img/resume-photo.jpg" alt="Photo of Gunaraj" />
      </div>
    </div>

    <div class="full-content">
      <!-- Work Experience -->
      <h2 class="section-heading cascade" style="--delay: 200ms;">Work Experience</h2>
      <div class="entry cascade" style="--delay: 250ms;">
        <h3>Unity Intern – Realfy Oasis Pvt Ltd</h3>
        <h4>Sep 2024 – March 2025</h4>
        <p>Developed a fitness app in Unity using MoveNet and implemented Firebase authentication, real-time DB integration, UI/UX animations, and fitness tracking features.</p>
        <div class="tech-stack">Unity, C#, MoveNet, Firebase, Google Fit API, DOTween, UI/UX</div>
      </div>

      <!-- Projects -->
      <h2 class="section-heading cascade" style="--delay: 300ms;">Projects</h2>
      <div class="entry cascade" style="--delay: 350ms;">
        <h3>Gravity Shift (Inspired by Sky Beneath)</h3>
        <h4>Sept 2024</h4>
        <p>Implemented a gravity-shifting system with smooth reorientation and character alignment. Puzzle-based mechanics and hologram previews.</p>
        <div class="tech-stack">Unity, C#, Rigidbody, Cinemachine</div>
      </div>

      <div class="entry cascade" style="--delay: 400ms;">
        <h3>Space Object Collector</h3>
        <h4>April 2025</h4>
        <p>Arcade-style 2D game where players collect floating space debris with limited resources and combo bonuses. Built with a clean MVC structure.</p>
        <div class="tech-stack">Unity, C#, MVC, Singleton, Object Pooling, Service Locator</div>
      </div>

      <!-- Skills -->
      <h2 class="section-heading cascade" style="--delay: 450ms;">Skills</h2>
      <div class="skill-set-container">
        <div class="skill-set cascade" style="--delay: 500ms;">
          <h3>Programming & Architecture</h3>
          <SkillRate name="C#" :rate="5" />
          <SkillRate name="OOP / Design Patterns" :rate="5" />
          <SkillRate name="Unity 2D/3D" :rate="5" />
          <SkillRate name="MVC / SOLID Principles" :rate="4" />
          <SkillRate name="C++ (Beginner)" :rate="2" />
        </div>

        <div class="skill-set cascade" style="--delay: 550ms;">
          <h3>Tools & Collaboration</h3>
          <SkillRate name="Git / GitHub" :rate="5" />
          <SkillRate name="Jira / Agile" :rate="4" />
          <SkillRate name="ClickUp / Miro" :rate="3" />
        </div>
      </div>

      <!-- Education -->
      <h2 class="section-heading cascade" style="--delay: 600ms;">Education</h2>
      <div class="entry cascade" style="--delay: 650ms;">
        <h3>St. Joseph Engineering College</h3>
        <h4>B.E. in Mechanical Engineering</h4>
        <div>Aug 2018 – Sept 2022</div>
      </div>

      <div class="entry cascade" style="--delay: 700ms;">
        <h3>Govt PU College Navunda</h3>
        <h4>PUC – PCMB</h4>
        <div>Jun 2016 – Mar 2018</div>
      </div>

      <!-- Certifications -->
      <h2 class="section-heading cascade" style="--delay: 750ms;">Certifications</h2>
      <div class="entry cascade" style="--delay: 800ms;">
        <h3>Foundational C# with Microsoft</h3>
        <div>Oct 2023</div>
        <h3>Unity 2D and C# for Beginner Game Developers</h3>
        <div>Jan 2023</div>
        <h3>3D Modelling and Texturing with Blender</h3>
        <div>Dec 2022</div>
      </div>

      <!-- Languages -->
      <h2 class="section-heading cascade" style="--delay: 850ms;">Languages</h2>
      <div class="entry cascade" style="--delay: 900ms;">
        <h3>English</h3>
        <div>Professional proficiency</div>
        <h3>Kannada, Hindi</h3>
        <div>Native proficiency</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Resume",
  mounted() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
});
</script>

<style scoped>
/* Typography & Layout */
body {
  font-family: 'Inter', sans-serif;
  background-color: #fff;
  color: #222;
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

.intro-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
  flex-wrap: wrap;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 10px;
}

.paragraph {
  flex: 1;
  min-width: 250px;
  font-size: 1.05rem;
  line-height: 1.7;
}

.resume-photo {
  flex-shrink: 0;
}

.resume-photo img {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-radius: 50%;
}

.download-wrapper {
  margin-top: 20px;
}

.download-link {
  color: #007bff;
  text-decoration: none;
  font-weight: 500;
}

.full-content {
  padding-top: 40px;
}

.section-heading {
  margin-top: 60px;
  padding-top: 20px;
  border-top: 1px solid #ccc;
  font-size: 1.5rem;
}

.entry {
  margin-bottom: 30px;
}

.entry h3 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 5px;
}

.entry h4 {
  font-size: 0.95rem;
  font-weight: 400;
  color: #888;
  margin-bottom: 10px;
}

.entry p {
  margin-bottom: 10px;
}

.tech-stack {
  font-size: 0.9rem;
  color: #555;
  font-style: italic;
}

/* Skills Grid */
.skill-set-container {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
}

/* Responsive */
@media (max-width: 768px) {
  .intro-container {
    flex-direction: column;
    text-align: center;
  }

  .resume-photo img {
    margin-top: 20px;
  }

  .skill-set-container {
    flex-direction: column;
  }
}
</style>