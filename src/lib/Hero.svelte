<script lang="ts">
  import { onMount } from 'svelte';
  
  let videoLoaded = false;
  
  onMount(() => {
    setTimeout(() => {
      videoLoaded = true;
    }, 100);
  });
</script>

<section class="relative h-screen flex items-center justify-center overflow-hidden">
  <!-- Background Image -->
  <div class="absolute inset-0 w-full h-full">
    <img
      class="object-cover w-full h-full"
      src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?auto=format&fit=crop&q=80"
      alt="Café interior"
    />
    <div class="absolute inset-0 bg-black/30"></div>
  </div>

  <!-- Content -->
  <div class="container relative z-10 text-white text-center px-4">
    <h1 class="text-4xl md:text-6xl font-bold mb-6 animate-fade-in">
      Welcome to Café Aroma
    </h1>
    <p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto animate-slide-up">
      Experience the finest coffee and homemade pastries in a cozy atmosphere
    </p>
    <a href="#menu" class="btn btn-primary text-lg animate-slide-up">
      View Our Menu
    </a>
  </div>

  <!-- Scroll Indicator -->
  <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
    </svg>
  </div>
</section>