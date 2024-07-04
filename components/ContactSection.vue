<template>
  <div class="contact-page">
    <h1 class="contact mb-5">Contact Us</h1>
    <div class="contact-form">
      <form @submit.prevent="submitForm">
        <input type="text" v-model="formData.name" placeholder="Your Name" required>
        <input type="email" v-model="formData.email" placeholder="Your Email" required>
        <textarea v-model="formData.message" placeholder="Your Message" rows="5" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        message: ''
      }
    };
  },
  methods: {
    submitForm() {
      // Handle form submission logic here
      console.log('Form submitted!', this.formData);
      // Example: You can add form submission logic using Axios or fetch API
    }
  }
};
</script>

<style scoped>
.contact-page {
  background: linear-gradient(90deg, rgba(0, 0, 50, 0.9), rgba(0, 0, 100, 0.9));
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #fff;
  padding: 20px;
}

.contact-form {
  width: 400px;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
  text-align: center;
  background-color: rgba(0, 0, 0, 0.5);
}

.contact-form h1 {
  margin-bottom: 20px;
}

.contact-form input[type="text"],
.contact-form input[type="email"],
.contact-form textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid #2e3648;
  background-color: rgba(46, 54, 72, 0.5);
  color: #fff;
  border-radius: 4px;
  transition: background-color 0.3s ease;
}

.contact-form input[type="text"]:focus,
.contact-form input[type="email"]:focus,
.contact-form textarea:focus {
  background-color: rgba(46, 54, 72, 0.8);
}

.contact-form button {
  background-color: #6e49ff;
  color: #fff;
  border: none;
  padding: 12px 20px;
  font-size: 16px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.contact-form button:hover {
  background-color: #8b65ff;
}

.contact{
  font-size: 1.8em;
    font-weight: bold;
    color: #00FFEE;
    text-decoration: none;
    text-shadow: 0 0 10px #00FFEE, 0 0 20px #00FFEE;
}
</style>


