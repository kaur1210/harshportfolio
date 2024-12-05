<template>
  <div class="hero-wrapper">
    <!-- Hero Section -->
    <div class="hero-image-container">
      <img :src="require('@/assets/Images/harshpreet.jpeg')" alt="Harshpreet's Portrait" class="hero-image">
    </div>
    <div class="hero-content text-center">
      <h1 class="display-6">Hi, I'm Harshpreet</h1>
      <p class="lead">Welcome to my portfolio! Explore my journey in photography, graphic design, and UI/UX design.</p>
      <hr class="my-4 mx-auto">
      <p>Discover my latest projects, skills, and design philosophy. Let's collaborate to create impactful visual and digital experiences.</p>
    </div>

    <!-- Journey Section -->
    <section class="my-journey py-5">
      <div class="container text-center">
        <h2 class="display-4 mb-4">My Journey in Photography and Digital Design</h2>
        <p class="lead">Creativity meets precision in my work, where visual storytelling drives innovation. From capturing moments to creating intuitive designs, I aim to deliver inspiring and engaging visual experiences.</p>
        <div class="row mt-5">
          <div class="col-md-4 mb-4">
            <h3>Photography</h3>
            <p>Photography is my passion and creative outlet. With experience in portrait, landscape, and event photography, I aim to tell stories through powerful visuals. I bring moments to life with attention.</p>
          </div>
          <div class="col-md-4 mb-4">
            <h3>Graphic Design</h3>
            <p>My design approach is rooted in clean aesthetics and intuitive interfaces. Using tools like Adobe Photoshop and Illustrator, I craft visually compelling graphics that communicate your brand story.</p>
          </div>
          <div class="col-md-4 mb-4">
            <h3>UX/UI Design</h3>
            <p>I specialize in user-centered design, focusing on creating smooth, engaging experiences. My goal is to make websites and apps not only beautiful but also intuitive and accessible to every user.</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>



<script>
export default {
  name: 'HeroSection',
};
</script>

<style scoped>
.f {
  color: #d2dde0 !important;
}

.hero-wrapper {
  display: flex;
  align-items: center;
  padding: 3rem; /* Increased padding for spacious layout */
  background-color: #2a3b3b; /* Slightly darker background for better contrast */
  border-radius: 16px;
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
  max-width: 1100px; /* Slightly increased max width */
  margin: 3rem auto;
  flex-wrap: wrap;
}

.hero-image-container {
  flex-shrink: 0;
  margin-right: 3rem;
  display: flex;
  justify-content: center;
}

.hero-image {
  width: 200px; /* Slightly larger image */
  height: 200px;
  object-fit: cover;
  border-radius: 50%;
  border: 6px solid #007bff; /* Thicker border for better emphasis */
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.hero-content {
  max-width: 650px; /* Increased width for better text space */
  text-align: left;
  color: #fff; /* White text for better readability */
}

.display-6 {
  font-size: 3.5rem; /* Larger heading */
  font-weight: 700;
  margin-bottom: 1rem;
}

.lead {
  font-size: 1.25rem;
  color: #d2dde0; /* Light grey color for the lead text */
  margin-bottom: 1.5rem;
}

hr.my-4 {
  border-top: 1px solid #ddd;
  margin: 1.5rem 0;
}

.view {
  background: linear-gradient(145deg, #6fa3d4, #4a7cbf);
  border: none;
  padding: 14px 28px;
  font-size: 1.2rem; /* Slightly larger font */
  font-weight: 600;
  color: #fff;
  border-radius: 50px;
  text-align: center;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease, color 0.3s ease;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
}

.view:hover {
  background: linear-gradient(145deg, #7eaecf, #5c88b3);
  transform: translateY(-6px);
  box-shadow: 0 16px 32px rgba(0, 0, 0, 0.15);
}

.view:focus {
  outline: none;
}

/* Responsive Styles */
@media (max-width: 1024px) {
  .hero-wrapper {
    flex-direction: column;
    padding: 2rem;
    margin: 2rem;
  }

  .hero-image-container {
    margin-right: 0;
    margin-bottom: 2rem;
  }

  .hero-image {
    width: 180px;
    height: 180px;
  }

  .display-6 {
    font-size: 2.75rem;
  }

  .lead {
    font-size: 1.15rem;
  }
}
/* General Styles */
.my-journey {
  padding: 60px 0;
  font-family: 'Roboto', sans-serif;
}

.my-journey .container {
  max-width: 1200px;
  margin: 0 auto;
}

.my-journey h2 {
  font-size: 3rem;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 30px;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.my-journey .lead {
  font-size: 1.25rem;
  color: #ffffff;
  max-width: 800px;
  margin: 0 auto 50px;
  line-height: 1.6;
  font-weight: 300;
}

.journey-card {
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.journey-card h3 {
  font-size: 1.75rem;
  color: #16a085;
  font-weight: 600;
  margin-bottom: 20px;
  text-transform: capitalize;
}

.journey-card p {
  font-size: 1rem;
  color: #7f8c8d;
  line-height: 1.6;
}

.journey-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
}

/* Responsive Design */
@media (max-width: 768px) {
  .my-journey h2 {
    font-size: 2.5rem;
  }

  .my-journey .lead {
    font-size: 1.1rem;
    max-width: 100%;
  }

  .journey-card {
    padding: 20px;
  }

  .journey-card h3 {
    font-size: 1.5rem;
  }

  .journey-card p {
    font-size: 0.95rem;
  }
}

/* Hover Effects for Buttons */
.journey-card:hover {
  background-color: #ecf9f5;
  border-left: 5px solid #16a085;
}

/* Mobile Friendly */
@media (max-width: 576px) {
  .my-journey h2 {
    font-size: 2rem;
  }

  .my-journey .lead {
    font-size: 1rem;
  }

  .journey-card {
    padding: 15px;
  }
}


@media (max-width: 768px) {
  .hero-wrapper {
    padding: 1.5rem;
  }

  .hero-image {
    width: 160px;
    height: 160px;
  }

  .display-6 {
    font-size: 2.25rem;
  }

  .lead {
    font-size: 1.1rem;
  }
}

@media (max-width: 480px) {
  .hero-wrapper {
    padding: 1rem;
  }

  .hero-image {
    width: 130px;
    height: 130px;
  }

  .display-6 {
    font-size: 1.8rem;
  }

  .lead {
    font-size: 1rem;
  }

  .view {
    font-size: 1rem;
    padding: 10px 22px;
  }
}
</style>
