<template>
    <div class="about-page">
      <h1>This is the About Page</h1>
      <div class="content">
        <h2>About Us</h2>
        <p>Welcome to our website. We are a team of dedicated professionals passionate about providing high-quality services.</p>
      </div>
      <div class="team">
        <h2>Our Team</h2>
        <ul>
          <li v-for="member in teamMembers" :key="member.id">{{ member.name }} - {{ member.position }}</li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'AboutPage',
    data() {
      return {
        teamMembers: [
          { id: 1, name: 'Nasir Hussain', position: 'CEO' },
          { id: 2, name: 'Sajid Alee', position: 'CTO' },
          { id: 3, name: 'Jaffar Ansari', position: 'Lead Developer' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  h1 {
    color: rebeccapurple;
    font-size: 28px;
  }
  
  .content {
    margin-bottom: 20px;
  }
  
  .team {
    margin-top: 40px;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    margin-bottom: 10px;
  }
  </style>
  