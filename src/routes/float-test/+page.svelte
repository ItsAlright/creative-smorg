<script>
  import { onMount } from 'svelte';
  
  let gameContainer;
  
  onMount(() => {
    // Create an iframe to host your game
    const iframe = document.createElement('iframe');
    iframe.src = '/float_test_1_1.html'; // Path to your HTML file in static folder
    iframe.style.width = '100%';
    iframe.style.height = '600px';
    iframe.style.border = 'none';
    
    // Append the iframe to the container
    gameContainer.appendChild(iframe);
  });
</script>

<div bind:this={gameContainer} class="game-container">
  <!-- Your game will be loaded here -->
</div>

<style>
  .game-container {
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
  }
</style>
