<template>
  <div class="projects-page container mt-5">
    <featured-projects :featuredProjects="projects" />
  </div>
</template>

<script>
import FeaturedProjects from '@/components/FeaturedProjects.vue';

export default {
  components: {
    FeaturedProjects
  },
  data() {
    return {
      projects: [
        {
          title: 'Portrait Perfection',
          description: 'A photography project focused on capturing expressive portraits with attention to lighting and composition.',
          image: require('@/assets/Images/IMG_0456 2.JPG'), 
          link: '#'
        },
        {
          title: 'Visual Vibes',
          description: 'A graphic design collection showcasing creative posters and branding materials for local events and businesses.',
          image: require('@/assets/Images/AI-projects3.jpg'), 
          link: '#'
        },
        {
          title: 'LensScapes',
          description: 'A landscape photography series exploring nature’s beauty with dynamic perspectives and vibrant colors.',
          image: require('@/assets/Images/flower.jpg'), 
          link: '#'
        },
        {
          title: 'UXFlow',
          description: 'A UI/UX design project focused on enhancing user experience for a mobile productivity app with intuitive navigation.',
          image: require('@/assets/Images/ui-banner.jpg'), 
          link: '#'
        },
        {
          title: 'Brand Identity Pro',
          description: 'A graphic design project delivering cohesive branding packages for startups, including logos and marketing materials.',
          image: require('@/assets/Images/logo.jpg'),  
          link: '#'
        },
        {
          title: 'GalleryEase',
          description: 'A curated photography platform designed to display artwork and photographs in an engaging online gallery format.',
          image: require('@/assets/Images/photo.jpg'), 
          link: '#'
        }
      ]
    };
  },
  head() {
    return {
      title: 'Projects - My Portfolio',
      meta: [
        { name: 'description', content: 'Explore my work in photography, graphic design, and UI/UX design that highlights creativity and user-centric solutions.' }
      ]
    };
  }
};
</script>


<style scoped>
.projects-page {
  max-width: 1200px;
  margin: auto;
}

h1, .card-title {
  font-weight: bold;
}

.card {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}

h1 {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  color: #b69928;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1); 
}

.card:hover {
  transform: scale(1.03);
}

.card-img-top {
  height: 200px;
  object-fit: cover;
}

.card-text {
  font-size: 0.9rem;
  color: #6c757d;
}

.btn-primary {
  background-color: #007bff;
  border-color: #007bff;
}


@media (min-width: 576px) {
  .card-columns {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }
}

@media (min-width: 768px) {
  .card-columns {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 992px) {
  .card-columns {
    grid-template-columns: repeat(4, 1fr);
  }
}

@media (min-width: 1200px) {
  .card-columns {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
