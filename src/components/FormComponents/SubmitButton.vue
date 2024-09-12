<template>
    <button class="submit-button" @click="$emit('click')">
      {{ text }}
    </button>
  </template>
  
  <script>
  export default {
    props: {
      text: String
    }
  }
  </script>
  
  <style scoped>
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
  </style>
  