<template>
    <header class="header">
      <img :src="logoSrc" alt="Hospital Logo" class="logo" />
      <h1 class="title">Our Hospital</h1>
      <nav>
        <ul class="nav-list">
          <li><a href="#about">About</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    props: {
      logoSrc: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .header {
    background-color: #4CAF50;
    color: white;
    padding: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .logo {
    height: 50px;
  }
  .title {
    margin: 0;
    font-size: 24px;
  }
  .nav-list {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
  }
  .nav-list li {
    margin-left: 20px;
  }
  .nav-list a {
    color: white;
    text-decoration: none;
  }
  .nav-list a:hover {
    text-decoration: underline;
  }
  </style>
  