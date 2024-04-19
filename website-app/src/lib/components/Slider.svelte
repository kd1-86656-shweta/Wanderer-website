<script>
    import { onMount, onDestroy } from 'svelte';
  
    let currentSlide = 1;
    const totalSlides = 5; // Adjust the total number of slides
  
    // Function to change the slide automatically
    function changeSlide() {
      if (currentSlide < totalSlides) {
        currentSlide += 1;
      } else {
        currentSlide = 1;
      }
    }
  
    // Automatic slide change interval (adjust the duration as needed)
    const interval = setInterval(changeSlide, 5000); // Change slide every 5 seconds
  
    // Clean up the interval on component destruction
    onDestroy(() => {
      clearInterval(interval);
    });
  </script>
  
  <style>
    /* Add your slider styles here */
    .slider {
      /* Styles for the slider container */
    }
  
    .slide {
      /* Styles for each slide */
    }
  </style>
  
  <div class="slider">
    <!-- Add your slides here, you can use Svelte logic to conditionally display content based on the currentSlide -->
    {#each Array(totalSlides) as _, index}
      <div bind:this={index} class="slide" style="display: {currentSlide === index + 1 ? 'block' : 'none'};">
        <!-- Content for each slide -->
        <p>Slide {index + 1}</p>
      </div>
    {/each}
  </div>
  