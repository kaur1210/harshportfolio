<template>
  <div class="skills-page mt-5">

    <div class="text-center mb-5">
      <h1 class="display-4">My Skills</h1>
      <p class="lead welcome-text">I specialize in crafting stunning visuals, intuitive designs, and user-friendly web applications. Below is an overview of my technical expertise and creative skills.</p>
      <hr class="my-4 mx-auto" style="width: 50%; border-top: 2px solid #0b72b9;">
    </div>

    <!-- Skills Overview Section -->
    <section class="skills-overview mb-5 p-4 shadow-lg rounded intro">
      <div class="section-header d-flex align-items-center mb-3">
        <h2 class="m-0 text-white">Key Skills</h2>
      </div>
      <p class="text-white">
        Over the years, I have developed expertise in photography, graphic design, and UI/UX design. My skillset bridges creative artistry with technical implementation, enabling me to deliver impactful visuals and interactive experiences.
      </p>
    </section>

    <!-- Skill Progress Bars Section -->
    <section class="skills-progress mb-5">
      <div v-for="skill in skills" :key="skill.name" class="skill-item mb-4">
        <div class="d-flex justify-content-between align-items-center">
          <h5 class="skill-name">{{ skill.name }}</h5>
          <span class="skill-level">{{ skill.level }}</span>
        </div>
        <div class="progress" style="height: 30px;">
          <div :style="{ width: skill.percent + '%' }" class="progress-bar" role="progressbar" :aria-valuenow="skill.percent" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section class="projects mb-5 p-4 shadow-lg rounded">
      <h3 class="text-center mb-4">Highlighted Projects</h3>
      <div class="project-item">
        <h5>Project 1: Photography Portfolio</h5>
        <p>A curated collection of my best photography work, capturing the essence of people, places, and moments through creative composition and lighting.</p>
      </div>
      <div class="project-item">
        <h5>Project 2: Graphic Design Collection</h5>
        <p>Featured branding and poster designs created using Adobe Illustrator and Photoshop, showcasing my ability to convey visual narratives through design.</p>
      </div>
      <div class="project-item">
        <h5>Project 3: UI/UX Design for Web Application</h5>
        <p>Designed and prototyped user-centric web applications using Figma and Adobe XD. Delivered intuitive user experiences focusing on functionality and aesthetics.</p>
      </div>
    </section>

  </div>
</template>


<script>
export default {
  data() {
    return {
      skills: [
        { name: 'Photography', level: 'Advanced', percent: 90 },
        { name: 'Graphic Design', level: 'Expert', percent: 95 },
        { name: 'UI/UX Design', level: 'Advanced', percent: 85 },
        { name: 'HTML5 & CSS3', level: 'Advanced', percent: 80 },
        { name: 'JavaScript & Vue.js', level: 'Intermediate', percent: 75 },
        { name: 'Adobe Suite', level: 'Expert', percent: 95 },
      ],
    };
  },
  head() {
    return {
      title: 'Skills - My Portfolio',
      meta: [
        { name: 'description', content: 'Explore my skills in photography, graphic design, UI/UX design, and web development.' },
      ],
    };
  },
};
</script>


<style scoped>
.skills-page {
  max-width: 1000px;
  margin: auto;
  padding: 20px;
}

h1, h2 {
  font-weight: bold;
}

.welcome-text {
  color: #ffffff !important;
  font-weight: 500;
  font-size: 1.3rem;
  line-height: 1.6;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
}

h1 {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  color: #ffffff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.display-4 {
  font-size: 2.5rem;
  font-weight: 600;
}

.lead {
  font-size: 1.25rem;
  color: #ffffff;
  font-weight: 500;
}

/* Skills Overview Section */
.skills-overview {
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.skills-overview h2 {
  font-size: 1.8rem;
  color: #ffffff;
  font-weight: 700;
}

.text-white {
  font-size: 1.1rem;
  color: #f8f9fa;
}

/* Skill Progress Bar */
.skill-item {
  padding: 10px 0;
}

.skill-name {
  font-size: 1.1rem;
  font-weight: 600;
  color: #0b72b9;
}

.skill-level {
  font-size: 1.1rem;
  color: #495057;
}

.progress-bar {
  background-color: #0b72b9;
  transition: width 1s ease-in-out;
}

.projects {
  background: #f1f3f5;
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.project-item h5 {
  font-size: 1.2rem;
  color: #0b72b9;
  font-weight: 700;
}

.project-item p {
  font-size: 1rem;
  color: #495057;
}

/* Button Style */
.btn-gradient {
  background: linear-gradient(45deg, #071c34, #A1CCDC);
  border: none;
  padding: 0.75rem;
  font-size: 1.1rem;
  text-align: center;
  color: white;
  transition: background 0.3s ease, transform 0.3s ease;
}

.btn-gradient:hover {
  background: linear-gradient(45deg, #A1CCDC, #071c34);
  transform: scale(1.05);
}

/* Media Queries for Responsive Design */
@media (max-width: 1200px) {
  .display-4 {
    font-size: 2.8rem;
  }

  .welcome-text {
    font-size: 1.1rem;
  }
}

@media (max-width: 992px) {
  .container {
    max-width: 90%;
  }

  .display-4 {
    font-size: 2.8rem;
  }

  .lead {
    font-size: 1.15rem;
  }

  .btn-lg {
    padding: 0.6rem 1.2rem;
  }
}

@media (max-width: 768px) {
  .skills-page {
    max-width: 100%;
    padding: 15px;
  }

  .welcome-text {
    font-size: 1.1rem;
  }

  .display-4 {
    font-size: 2.5rem;
  }

  .lead {
    font-size: 1rem;
  }

  .btn-lg {
    padding: 0.5rem 1rem;
  }
}

@media (max-width: 576px) {
  .display-4 {
    font-size: 2.2rem;
  }

  .lead {
    font-size: 0.9rem;
  }

  .btn-lg {
    padding: 0.4rem 0.8rem;
    font-size: 0.9rem;
  }

  .container {
    padding-left: 15px;
    padding-right: 15px;
  }
}
</style>
