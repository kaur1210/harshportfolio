<!-- pages/index.vue -->
<template>
    <div class="background">
      <HeroSection />
      <FeaturedProjects :featuredProjects="featuredProjects" />
      <SkillsSection :skills="skills" />
      
    </div>
  </template>
  
  <script>
  import HeroSection from '~/components/HeroSection.vue';
  import FeaturedProjects from '~/components/FeaturedProjects.vue';
  import SkillsSection from '~/components/SkillsSection.vue';
 
  export default {
    components: {
      HeroSection,
      FeaturedProjects,
      SkillsSection,
      
    },
   
  data() {
    return {
      featuredProjects: [
      {
          id: 1,
          title: 'Photography',
          description: 'A curated gallery showcasing my photography projects, capturing moments and stories through a creative lens.',
          image: require('@/assets/Images/photography-banner.jpg'), 
          link: '#'
        },  
      {
          id: 2,
          title: 'Graphic Design',
          description: 'A collection of graphic design projects, including branding, posters, and digital art created using Adobe Suite and Figma',
          image: require('@/assets/Images/graphic-banner.jpg'),  
          link: '#'
        },
        {
          id: 3,
          title: 'UI/UX Design',
          description: 'A portfolio of UI/UX design projects, featuring designs, mobile applications using tools like Figma and Adobe XD.',
          image: require('@/assets/Images/ui-banner.jpg'), 
          link: '#'
        }
      
      ],
      skills: [
        { name: 'Photography', level: 'Expert', percent: '85' },
        { name: 'Graphic designer', level: 'Expert', percent: '80' },
        { name: 'UI/UX designs', level: 'Advanced', percent: '75' },
        
      
      ],

    };
  }
};

  </script>
  