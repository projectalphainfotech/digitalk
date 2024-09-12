<template>
  <div class="landing-page">
    <header class="header">
      <img src="https://placehold.co/600x400" alt="Hospital Logo" class="logo" />
      <h1 class="main-title">Welcome</h1>
      <p class="intro-text">We're here to assist you with all your needs. Please fill out the form below to
        get in touch with us.</p>
    </header>
    <section class="contact-form-section">
      <div class="simple-form">
        <form @submit.prevent="handleSubmit">
          <h1></h1>
          <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" id="name" v-model="form.name" placeholder="Enter your name" required />
          </div>
          <div class="form-group">
            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" v-model="form.phone" placeholder="Enter your phone number" required />
          </div>

          <div class="form-group">
            <label for="city">City:</label>
            <input type="text" id="city" v-model="form.city" placeholder="Enter your city" required />
          </div>
          <div class="form-group">
            <label for="choice1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi, tenetur!</label>
            <input type="text" id="choice1" v-model="form.choice1" placeholder="Enter first choice" />
          </div>
          <div class="form-group">
            <label for="choice2">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Non, quibusdam.</label>
            <input type="text" id="choice2" v-model="form.choice2" placeholder="Enter second choice" />
          </div>
          <button type="submit" class="submit-button">Call Me Back</button>
        </form>
      </div>
    </section>
    <footer class="footer">
      <p>&copy; 2024.All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        phone: '',
        city: '',
        choice1: '',
        choice2: ''
      }
    };
  },
  methods: {
    handleSubmit() {
      // Handle form submission
      alert(`Name: ${this.form.name}\nPhone: ${this.form.phone}\nCity: ${this.form.city}\nChoice 1: ${this.form.choice1}\nChoice 2: ${this.form.choice2}`);
    }
  }
};
</script>

<style scoped>
html,
body {
  height: 100%;
  width: 100%;
  margin: 0;
  font-family: Arial, sans-serif;
}

.landing-page {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.header {
  text-align: center;
  padding: 40px;
  background-color: #f4f4f4;
}

.logo {
  display: block;
  height: 150px;
  border-radius: 50px;
}


/* .logo {
  display: block;
  margin: 0 auto 20px;
  height: 150px;
  border-radius: 100px;
} */


.main-title {
  font-size: 36px;
  margin-bottom: 10px;
}

.intro-text {
  font-size: 18px;
  color: #555;
}

.contact-form-section {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.form-title {
  text-align: center;
  margin-bottom: 20px;
  font-size: 24px;
}

.simple-form {
  margin:50px;
  max-width: 500px;
  width: 100%;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
}

.form-group input {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.submit-button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.submit-button:hover {
  background-color: #45a049;
}

.footer {
  text-align: center;
  padding: 10px;
  background-color: #f4f4f4;
  border-top: 1px solid #ccc;
}
</style>
