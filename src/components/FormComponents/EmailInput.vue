<template>
    <div class="email-input">
      <label :for="id">{{ label }}</label>
      <input
        type="email"
        :id="id"
        :placeholder="placeholder"
        v-model="value"
      />
    </div>
  </template>
  
  <script>
  export default {
    props: {
      id: String,
      label: String,
      placeholder: String,
      value: String
    }
  }
  </script>
  
  <style scoped>
  .email-input {
    margin-bottom: 16px;
  }
  .email-input label {
    display: block;
    margin-bottom: 8px;
    font-weight: bold;
  }
  .email-input input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  </style>
  