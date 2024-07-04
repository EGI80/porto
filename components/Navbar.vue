<template>
    <nav class="navbar">
      <div class="container">
        <a href="/" class="logo">MyApp</a>
        <ul class="nav-links">
          <li class="nav-item">
            <a href="#hero" class="nav-link">Home</a>
          </li>
          <li class="nav-item">
            <a href="#about" class="nav-link">About</a>
          </li>
          <li class="nav-item">
            <a href="#project" class="nav-link">Projects</a>
          </li>
          <li class="nav-item">
            <a href="#contact" class="nav-link">Contact</a>
          </li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar'
  }
  </script>
  
  <style scoped>
  .navbar {
    background: linear-gradient(90deg, rgba(0, 0, 50, 0.9), rgba(0, 0, 100, 0.9));
    border-bottom: 2px solid #dc3545;
    padding: 15px 0;
  }
  
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo {
    font-size: 1.8em;
    font-weight: bold;
    color: #00FFEE;
    text-decoration: none;
    text-shadow: 0 0 10px #00FFEE, 0 0 20px #00FFEE;
  }
  
  .nav-links {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
  }
  
  .nav-item {
    margin-left: 20px;
  }
  
  .nav-link {
    color: #FFF;
    text-decoration: none;
    transition: color 0.3s, text-shadow 0.3s;
    position: relative;
  }
  
  .nav-link:hover {
    color: #dc3545;
    text-shadow: 0 0 5px #dc3545, 0 0 10px #dc3545;
  }
  </style>
  