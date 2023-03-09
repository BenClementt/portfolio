<script>
  import Hero from './lib/Hero.svelte'
  import About from './lib/About.svelte'

  function scrollToAbout() {
    const about = document.querySelector('#about')
    about.scrollIntoView({ behavior: 'smooth' })
  }

</script>

<svelte:head>
  <title>Ben Clement Lighting</title>
  <meta name="description" content="" />
  <link rel="icon" type="image/png" href="/favicon.png" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
  <link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@200;300;400;500;600;700;800;900&amp;display=swap" rel="stylesheet">
  
</svelte:head>

  <div class="page" id="hero">
    <Hero />
  </div>
  <button class="scroll__arrow" on:click={scrollToAbout} on:keydown={scrollToAbout}>
    <svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-down-circle"><polyline points="8 12 12 16 16 12"></polyline><line x1="12" y1="8" x2="12" y2="16"></line></svg>
  </button>
  <div class="page" id="about">
    <About />
  </div>
