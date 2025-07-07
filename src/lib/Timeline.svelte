<script>
    export let items = [];
  </script>
  
  <div class="journey-timeline">
    {#each items as item}
      <div class="timeline-item">
        <div class="timeline-year">{item.year}</div>
        <div class="timeline-description">{item.description}</div>
      </div>
    {/each}
  </div>
  
  <style>
    .journey-timeline {
      position: relative;
      padding-left: 30px;
    }
  
    .journey-timeline::before {
      content: '';
      position: absolute;
      left: 15px;
      top: 0;
      bottom: 0;
      width: 2px;
      background: linear-gradient(to bottom, #00d0ee, #7ff889);
    }
  
    .timeline-item {
      position: relative;
      margin-bottom: 30px;
      padding-left: 30px;
    }
  
    .timeline-item::before {
      content: '';
      position: absolute;
      left: -8px;
      top: 5px;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      background: #00d0ee;
      border: 3px solid white;
      box-shadow: 0 2px 10px rgba(0,0,0,0.2);
    }
  
    .timeline-year {
      font-weight: bold;
      color: #2d3436;
      font-size: 1.1em;
    }
  
    .timeline-description {
      color: #636e72;
      margin-top: 5px;
    }
  </style>
  