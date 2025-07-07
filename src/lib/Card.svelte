<script>
    export let title;
  </script>
  
  <div class="card">
    <h2>{title}</h2>
    <slot />
  </div>
  
  <style>
    .card {
      background: rgba(255,255,255,0.9);
      border-radius: 20px;
      padding: 30px;
      margin-bottom: 30px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.3);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
  
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 40px rgba(0,0,0,0.2);
    }
  
    h2 {
      color: #2d3436;
      margin-bottom: 15px;
      font-size: 1.8em;
      display: flex;
      align-items: center;
      gap: 10px;
    }
  
    h2::before {
      content: "✨";
      animation: sparkle 2s infinite;
    }
  
    @keyframes sparkle {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
  </style>
  