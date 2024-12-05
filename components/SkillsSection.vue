<template>
  <div class="skills-container">
    <h2 class="text-center mb-5">My Skills</h2>
    <div class="skills-grid">
      <div
        class="skill-item"
        v-for="skill in skills"
        :key="skill.name"
        @mouseenter="startAnimation(skill)"
        @mouseleave="resetAnimation(skill)"
      >
        <div class="progress-ring">
          <svg class="circle" viewBox="0 0 120 120">
            <circle class="circle-background" cx="60" cy="60" r="54" stroke-width="12" />
            <circle
              class="circle-progress"
              cx="60"
              cy="60"
              r="54"
              stroke-width="12"
              stroke="#6c8eaf"
            />
          </svg>
          <div class="percentage">{{ skill.percent }}%</div>
        </div>
        <i :class="['mb-3', skill.icon, 'skill-icon']"></i>
        <h5 class="skill-name">{{ skill.name }}</h5>
        <p class="skill-level">{{ skill.level }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SkillsSection',
  props: {
    skills: Array,
  },
  data() {
    return {
      hoveredSkill: null,
    };
  },
  methods: {
    startAnimation(skill) {
      this.hoveredSkill = skill.name;
    },
    resetAnimation() {
      this.hoveredSkill = null;
    },
  },
};
</script>

<style scoped>
.skills-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  min-height: 100vh;
  padding: 20px;
}

h2 {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  color: #2c3e50;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
  letter-spacing: 1px;
  margin-bottom: 2rem;
}

.skills-grid {
  display: flex;
  justify-content: center;
  gap: 3rem;
  width: 100%;
}

.skill-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.progress-ring {
  position: relative;
  width: 120px;
  height: 120px;
  margin: 1rem auto;
  border-radius: 50%;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease, filter 0.3s ease;
}

.progress-ring:hover {
  transform: translateY(-12px) scale(1.05);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
  filter: brightness(1.1);
}

.circle-background {
  fill: none;
  stroke: #e1e1e1;
}

.circle-progress {
  fill: none;
  stroke-linecap: round;
  stroke: #3498db;
  transition: stroke-dashoffset 1s ease;
}

.percentage {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 1.5rem;
  font-weight: bold;
  color: #2c3e50;
}

.skill-icon {
  font-size: 2.2rem;
  color: #6c8eaf;
  margin-top: 10px;
  transition: color 0.3s ease, transform 0.3s ease;
}

.skill-icon:hover {
  color: #3498db;
  transform: scale(1.15);
}

.skill-name {
  font-size: 1.3rem;
  font-weight: 600;
  color: #2c3e50;
  margin-top: 10px;
}

.skill-level {
  font-size: 1rem;
  color: #7f8c8d;
  margin-top: 5px;
}

@media (max-width: 768px) {
  .progress-ring {
    width: 100px;
    height: 100px;
  }

  .skill-name {
    font-size: 1.1rem;
  }

  .skill-icon {
    font-size: 1.8rem;
  }
}

@media (max-width: 576px) {
  .skills-grid {
    flex-direction: column;
    align-items: center;
  }

  .progress-ring {
    width: 80px;
    height: 80px;
  }

  .skill-name {
    font-size: 1rem;
  }

  .skill-icon {
    font-size: 1.6rem;
  }
}
</style>
