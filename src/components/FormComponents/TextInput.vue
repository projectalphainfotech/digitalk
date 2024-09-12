<template>
    <div class="text-input">
      <label :for="id">{{ label }}</label>
      <input
        type="text"
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
  .text-input {
    margin-bottom: 16px;
  }
  .text-input label {
    display: block;
    margin-bottom: 8px;
    font-weight: bold;
  }
  .text-input input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  </style>
  