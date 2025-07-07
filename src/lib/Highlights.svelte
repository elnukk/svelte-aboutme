<script>
    export let highlights = [];
  </script>
  
  <div class="highlights">
    {#each highlights as h}
      <div class="highlight-item">
        <span class="highlight-icon">{h.icon}</span>
        <strong>{h.title}</strong><br />
        {h.text}
      </div>
    {/each}
  </div>
  
  <style>
    .highlights {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }
  
    .highlight-item {
      background: linear-gradient(45deg, #00d0ee, #7ff889);
      border-radius: 15px;
      padding: 20px;
      text-align: center;
      color: white;
      transition: transform 0.3s ease;
      cursor: pointer;
      position: relative;
      overflow: hidden;
    }
  
    .highlight-item::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
      transform: rotate(45deg);
      transition: transform 0.5s ease;
    }
  
    .highlight-item:hover::before {
      transform: rotate(45deg) translate(50%, 50%);
    }
  
    .highlight-item:hover {
      transform: translateY(-5px);
    }
  
    .highlight-icon {
      font-size: 2.5em;
      margin-bottom: 10px;
      display: block;
    }
  </style>
  