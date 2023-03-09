<script>
  import { onMount } from 'svelte';

  // add animations
  onMount(() => {
    const heroBg = document.querySelector('.hero__bg');
    const heroContent = document.querySelector('.hero__content');
    const heroTitle = document.querySelector('.hero__title');
    const heroSubtitle = document.querySelector('.hero__subtitle');

    /* Hero BG Animation */
    heroBg.classList.add('animate__animated', 'animate__fadeIn', 'animate__slow');
    heroContent.classList.add('animate__animated', 'animate__fadeInUp', 'animate__slow');
    heroTitle.classList.add('animate__animated', 'animate__fadeInDown', 'animate__slow');
    heroSubtitle.classList.add('animate__animated', 'animate__fadeInUp', 'animate__slow');
  });


  let heroTitle = 'Ben Clement';
  let heroSubtitle = 'Freelance Lighting Designer & Multi-Skilled Technician';
  
</script>

<style>
  * {
    box-sizing: border-box;
    font-family: 'Unbounded', sans-serif;
  }

.hero__bg{
  background-image: url("/images/hero.jpg");
  background-position: 70% 50%;
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

.hero__title{
  font-size: 3rem;
  font-weight: 600;
  color: #fff;
  text-align: center;
}

.hero__subtitle{
  font-size: 1rem;
  font-weight: 400;
  color: #fff;
  text-align: center;
}

</style>

<div class="hero__bg blur-xl"></div>
<div class="hero__content">
  <h1 class="hero__title">{heroTitle}</h1>
  <p class="hero__subtitle mt-2">{heroSubtitle}</p>
</div>