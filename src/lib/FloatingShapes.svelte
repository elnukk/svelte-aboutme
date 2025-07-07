<script>
    const shapes = ["🌸", "🦋", "✨", "🌙"];
  </script>
  
  <div class="floating-elements">
    {#each shapes as shape, i}
      <div class="floating-shape shape-{i + 1}">{shape}</div>
    {/each}
  </div>
  
  <style>
    .floating-elements {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      pointer-events: none;
      z-index: 0;
    }
  
    .floating-shape {
      position: absolute;
      opacity: 0.1;
      animation: float 6s ease-in-out infinite;
    }
  
    .shape-1 { top: 10%; left: 10%; animation-delay: 0s; }
    .shape-2 { top: 20%; right: 10%; animation-delay: 2s; }
    .shape-3 { bottom: 20%; left: 20%; animation-delay: 4s; }
    .shape-4 { bottom: 10%; right: 20%; animation-delay: 1s; }
  
    @keyframes float {
      0%, 100% { transform: translateY(0) rotate(0deg); }
      50% { transform: translateY(-20px) rotate(180deg); }
    }
  </style>
  