<template>
  <div class="container my-5">
    <h2 class="text-center display-3 mb-4 text-white"> Projects</h2>
    <div class="row">
      <div class="col-lg-4 col-md-6 col-sm-12 mb-4" v-for="project in featuredProjects" :key="project.id">
        <div class="project-card shadow-lg rounded overflow-hidden">
          <img :src="project.image" class="card-img-top" :alt="project.title">
          <div class="card-body">
            <h5 class="card-title text-center">{{ project.title }}</h5>
            <p class="card-text text-center">{{ project.description }}</p>
           </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FeaturedProjects',
  props: {
    featuredProjects: Array
  }
};
</script>

<style scoped>
.container {
  max-width: 1200px;
}

h2 {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  color: #b69928;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.project-card {
  transition: transform 0.4s ease, box-shadow 0.4s ease, border-color 0.4s ease;
  border: 1px solid #ddd;
  border-radius: 10px;
  overflow: hidden;
  background-color: #242e2e; /* Subtle dark background */
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 18px 38px rgba(0, 0, 0, 0.2);
  border-color: #007bff;
}

.project-card img {
  object-fit: cover;
  height: 220px; /* Increased image height for better visual impact */
}

.card-body {
  padding: 1.5rem;
  background-color: #2a3b3b; /* Slightly darker background */
  color: #f8f9fa; /* Text color for contrast */
}

.card-title {
  font-size: 1.35rem; /* Slightly larger font size for titles */
  font-weight: 700;
  color: #fff;
  margin-bottom: 0.75rem;
}

.card-text {
  color: #d0d6e2;
  font-size: 1rem;
  margin-bottom: 1.5rem;
}

.btn-gradient {
  background: linear-gradient(45deg, #ffffff, #ffffff);
  border: none;
  padding: 0.75rem;
  font-size: 1.1rem;
  font-weight: 600;
  color: rgb(0, 0, 0);
  text-align: center;
  transition: background 0.3s ease, transform 0.3s ease;
  border-radius: 50px; /* Rounded button corners */
}

.btn-gradient:hover {
  background: linear-gradient(45deg, #000000, #000000);
  color: rgb(255, 255, 255);
  transform: scale(1.05);
}

@media (max-width: 1199px) {
  .container {
    padding-left: 1.5rem;
    padding-right: 1.5rem;
  }

  .project-card img {
    height: 200px;
  }

  .card-body {
    padding: 1.25rem;
  }
}

@media (max-width: 991px) {
  .project-card img {
    height: 180px;
  }

  .card-body {
    padding: 1rem;
  }

  .btn-gradient {
    font-size: 1rem;
  }
}

@media (max-width: 767px) {
  h2 {
    font-size: 1.75rem;
  }

  .card-body {
    padding: 1rem;
  }

  .btn-gradient {
    font-size: 1rem;
  }

  .project-card img {
    height: 160px;
  }
}

@media (max-width: 576px) {
  h2 {
    font-size: 1.5rem;
  }

  .project-card img {
    height: 140px;
  }

  .btn-gradient {
    font-size: 0.9rem;
  }
}
</style>
