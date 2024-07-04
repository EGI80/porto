<template>
    <footer class="footer">
      <div class="container">
        
        <p class="footer-text">© 2024 MyApp. All rights reserved.</p>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer'
  }
  </script>
  
  <style scoped>
  .footer {
    background-color: #0C1844;
    color: #fff;
    padding: 20px 0;
  }
  
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .footer-content {
    display: flex;
    align-items: center;
  }
  
  .logo {
    font-size: 1.5em;
    font-weight: bold;
    color: #fff;
    text-decoration: none;
  }
  
  .footer-links ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
  }
  
  .footer-links li {
    margin-right: 20px;
  }
  
  .footer-links a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .footer-links a:hover {
    color: #dc3545; /* Warna merah sebagai warna bahaya */
  }
  
  .footer-text {
    margin-top: 10px;
    text-align: center;
    font-size: 0.9em;
  }
  </style>
  