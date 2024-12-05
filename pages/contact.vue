<template>
  <div class="contact-page container mt-5">
    <div class="text-center mb-5">
      <h1 class="display-3 text-white">Get in Touch</h1>
      <p class="lead contact-text">I'm always open to new opportunities, questions, and collaborations. Let's connect!</p>
      <hr class="my-4">
    </div>

    <div class="row">
      <!-- Contact Form -->
      <div class="col-12 col-md-6">
        <form @submit.prevent="submitForm" class="form-container shadow-lg p-4">
          <div class="form-group">
            <label for="name">Your Name</label>
            <input type="text" id="name" v-model="form.name" class="form-control" placeholder="Enter your full name" required />
          </div>
          <div class="form-group">
            <label for="email">Your Email</label>
            <input type="email" id="email" v-model="form.email" class="form-control" placeholder="Your email address" required />
          </div>
          <div class="form-group">
            <label for="phone">Phone Number</label>
            <input type="tel" id="phone" v-model="form.phone" class="form-control" placeholder="Your phone number" />
          </div>
          <div class="form-group">
            <label for="message">Your Message</label>
            <textarea id="message" v-model="form.message" class="form-control" rows="5" placeholder="What would you like to discuss?" required></textarea>
          </div>
          <div class="form-group">
            <label for="purpose">Purpose of Contact</label>
            <select id="purpose" v-model="form.purpose" class="form-control">
              <option value="General Inquiry">General Inquiry</option>
              <option value="Business Inquiry">Business Inquiry</option>
              <option value="Support">Support</option>
              <option value="Collaboration">Collaboration</option>
            </select>
          </div>
          <button type="submit" class="btn btn-gradient btn-block">Send Message</button>
        </form>
      </div>

      <!-- Contact Details with Purpose Options -->
      <div class="col-12 col-md-6 mt-4 mt-md-0">
        <div class="contact-details shadow-lg p-4">
          <h5 class="text-white">Other Ways to Reach Me</h5>
          <p>If you're looking for a faster response or want to connect directly, here are other options:</p>

          <ul class="contact-options">
            <li><strong>Email:</strong> <a href="mailto:support@example.com" class="text-light">support@example.com</a></li>
            <li><strong>Phone:</strong> <a href="tel:+1234567890" class="text-light">+1 (234) 567-890</a></li>
            <li><strong>Social Media:</strong> Follow me for updates:</li>
          </ul>
        
        </div>
      </div>
    </div>

    <!-- Quick Contact Information with Purpose -->
    <div class="quick-contact mt-5 text-center">
      <h4 class="text-dark">Not sure how to get in touch? Here are some options:</h4>
      <p>For technical questions, please email <a href="mailto:support@example.com" class="text-info">support@example.com</a>.</p>
      <p>For business inquiries, reach out to me via <a href="mailto:business@example.com" class="text-info">business@example.com</a>.</p>
      <p>For collaborations, connect on my <a href="https://linkedin.com/in/your-profile" class="text-info">LinkedIn</a> page.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        phone: '',
        message: '',
        purpose: 'General Inquiry',
      }
    };
  },
  methods: {
    submitForm() {
      alert(`Thank you, ${this.form.name}! Your message has been sent.`);
      this.form.name = '';
      this.form.email = '';
      this.form.phone = '';
      this.form.message = '';
      this.form.purpose = 'General Inquiry';
    }
  },
  head() {
    return {
      title: 'Contact Me - Get In Touch',
      meta: [
        { name: 'description', content: 'Reach out for inquiries, support, or collaboration opportunities.' }
      ]
    };
  }
};
</script>

<style scoped>
.contact-page {
  max-width: 900px;
  margin: auto;
  font-family: 'Roboto', sans-serif;
}

hr {
  border-width: 3px;
  border-color: #5c7a8c;
  width: 50px;
}

.contact-text {
  color: #ffffff;
  font-weight: 500;
  font-size: 1.3rem;
  line-height: 1.6;
}

h1 {
  font-weight: 700;
  color: #b69928;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.form-container {
  background-color: #463e3e;
  border-radius: 10px;
}

.form-control {
  border-radius: 0.5rem;
  margin-bottom: 1rem;
  box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.1);
}

.form-group label {
  color: #ffffff;
  font-weight: bold;
}

.btn-gradient {
  background: linear-gradient(45deg, #000000, #4e79b5);
  border: none;
  color: rgb(255, 255, 255);
  padding: 12px 20px;
  font-size: 1.1rem;
  text-align: center;
  text-transform: uppercase;
  border-radius: 0.5rem;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.btn-gradient:hover {
  transform: scale(1.05);
}

.contact-details {

  background-color: #463e3e;
  border-radius: 10px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.contact-details h5 {
  color: #fff;
  font-weight: 600;
}

.contact-details p {
  color: #ddd;
  font-size: 1rem;
}

.contact-options {
  list-style-type: none;
  padding: 0;
}

.contact-options li {
  color: #ddd;
  font-size: 1rem;
}

.contact-options a {
  color: #80b6c7;
  text-decoration: none;
}

.social-links a {
  margin-right: 0.5rem;
  font-size: 1rem;
}

.btn-social {
  display: inline-block;
  padding: 10px 20px;
  text-align: center;
  font-size: 1rem;
  color: white;
  border-radius: 0.5rem;
  transition: all 0.3s ease;
}

.btn-linkedin {
  background-color: #0077b5;
}

.btn-github {
  background-color: #333;
}

.btn-twitter {
  background-color: #1da1f2;
}

.btn-social:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.quick-contact {
  background-color: #f7f7f7;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.quick-contact a {
  color: #1da1f2;
  text-decoration: none;
}

.quick-contact a:hover {
  text-decoration: underline;
}

@media (max-width: 767px) {
  .contact-page {
    padding: 20px;
  }

  .row {
    flex-direction: column;
  }

  .contact-details {
    margin-top: 20px;
  }

  .social-links {
    display: flex;
    flex-wrap: wrap;
  }

  .btn-social {
    margin-bottom: 10px;
  }

  .contact-text {
    font-size: 1.1rem;
  }

  h1 {
    font-size: 2rem;
  }
}

@media (min-width: 768px) and (max-width: 1024px) {
  .contact-page {
    padding: 20px;
  }

  .row {
    flex-direction: row;
  }

  .contact-details {
    margin-top: 20px;
  }
}
</style>
