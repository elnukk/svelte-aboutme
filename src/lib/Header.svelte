<script>
    export let name;
    export let tagline;
  
  </script>
  
  <header class="header">
    <h1 class="name">{name}</h1>
    <p class="tagline">{tagline}</p>
  </header>
  
  <style>
    .header {
      text-align: center;
      margin-bottom: 60px;
      padding: 40px 0;
    }
  
    .name {
      font-size: 3.5em;
      color: #2d3436;
      margin-bottom: 10px;
      text-shadow: 2px 2px 0 rgba(255,255,255,0.3);
      cursor: pointer;
      transition: transform 0.3s ease;
    }
  
    .name:hover {
      transform: scale(1.05) rotate(2deg);
    }
  
    .tagline {
      font-size: 1.2em;
      color: white;
      font-style: italic;
    }
  </style>
  