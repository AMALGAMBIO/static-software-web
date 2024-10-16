<!-- App.vue -->
<template>
    <div id="app">
      <header>
        <h1>Amalgam Energy</h1>
        <nav>
          <a href="#about">About</a>
          <a href="#services">Services</a>
          <a href="#community-battery">Community Battery</a>
          <a href="#green-finance">Green Finance</a>
          <a href="#contact">Contact</a>
        </nav>
      </header>
  
      <main>
        <section id="hero">
          <h2>Powering Communities with Green Energy Solutions</h2>
          <p>Join the energy revolution with Amalgam Energy's community battery and green finance options.</p>
          <button @click="scrollTo('community-battery')">Learn More</button>
        </section>
  
        <section id="about">
          <h2>About Amalgam Energy</h2>
          <p>We are pioneering sustainable energy solutions that empower communities and individuals to take control of their energy future.</p>
        </section>
  
        <section id="services">
          <h2>Our Services</h2>
          <ul>
            <li>Community Battery Solutions</li>
            <li>Green Finance Options</li>
            <li>Prosumer Energy Management</li>
            <li>Investor Opportunities</li>
          </ul>
        </section>
  
        <section id="community-battery">
          <h2>Community Battery</h2>
          <p>Our innovative community battery system allows neighborhoods to store and share excess renewable energy, reducing costs and increasing energy independence.</p>
        </section>
  
        <section id="green-finance">
          <h2>Green Finance</h2>
          <p>We offer flexible financing options to make sustainable energy accessible to all. Invest in a greener future while enjoying attractive returns.</p>
        </section>
  
        <section id="contact">
          <h2>Contact Us</h2>
          <form @submit.prevent="submitForm">
            <input v-model="name" type="text" placeholder="Your Name" required>
            <input v-model="email" type="email" placeholder="Your Email" required>
            <textarea v-model="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send</button>
          </form>
        </section>
      </main>
  
      <footer>
        <p>&copy; 2024 Amalgam Energy. All rights reserved.</p>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        name: '',
        email: '',
        message: ''
      }
    },
    methods: {
      scrollTo(id) {
        const element = document.getElementById(id);
        element.scrollIntoView({ behavior: 'smooth' });
      },
      submitForm() {
        // Here you would typically send the form data to a server
        console.log('Form submitted', { name: this.name, email: this.email, message: this.message });
        alert('Thank you for your message. We will get back to you soon!');
        this.name = '';
        this.email = '';
        this.message = '';
      }
    }
  }
  </script>
  
  <style>
  #app {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
  }
  
  header {
    background-color: #2c3e50;
    color: white;
    padding: 1rem;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
  }
  
  nav a {
    color: white;
    text-decoration: none;
    margin-right: 1rem;
  }
  
  main {
    padding-top: 60px;
  }
  
  section {
    padding: 2rem;
    margin: 1rem 0;
  }
  
  #hero {
    background-color: #27ae60;
    color: white;
    text-align: center;
    padding: 4rem 2rem;
  }
  
  button {
    background-color: #3498db;
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    cursor: pointer;
    font-size: 1rem;
  }
  
  form {
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: 0 auto;
  }
  
  input, textarea {
    margin-bottom: 1rem;
    padding: 0.5rem;
  }
  
  footer {
    background-color: #34495e;
    color: white;
    text-align: center;
    padding: 1rem;
    position: relative;
    bottom: 0;
    width: 100%;
  }
  </style>