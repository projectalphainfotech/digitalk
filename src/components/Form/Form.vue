<template>
    <form @submit.prevent="handleSubmit">
      <TextInput
        id="name"
        label="Name"
        placeholder="Enter your name"
        v-model="form.name"
      />
      <EmailInput
        id="email"
        label="Email"
        placeholder="Enter your email"
        v-model="form.email"
      />
      <SubmitButton text="Submit" @click="handleSubmit" />
    </form>
  </template>
  
  <script>
  import TextInput from '../FormComponents/TextInput.vue'
  import EmailInput from '../FormComponents/EmailInput.vue'
  import SubmitButton from '../FormComponents/SubmitButton.vue'
  
  export default {
    components: {
      TextInput,
      EmailInput,
      SubmitButton
    },
    data() {
      return {
        form: {
          name: '',
          email: ''
        }
      }
    },
    methods: {
      handleSubmit() {
        // Handle form submission
        alert(`Name: ${this.form.name}\nEmail: ${this.form.email}`)
      }
    }
  }
  </script>
  
  <style scoped>
  form {
    max-width: 400px;
    margin: auto;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
  }
  </style>
  