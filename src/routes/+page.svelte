<script>
  import Resume from '$lib/assets/ShaneMisraATS.pdf'
	import Pic from '$lib/assets/Shane_Profile.jpg'

  let projects = {
    'Avian Anthems' : 'https://avian-anthems.vercel.app/',
    'Mars Chronicles' : 'https://mars-chronicles.vercel.app/',
    'Hyper Loom' : 'https://hyper-loom-explorer.vercel.app/'
  }

</script>

<header class='portfolio-header'>
  <h1 class='header-text'>Welcome to my Professional Portfolio!</h1>
  <ul class='header-link-container'>
    <li class='header-link'>Projects</li>
    <li class='header-link'>Idle Thoughts / Blog</li>
    <li class='header-link'>About Me</li>
  </ul>
</header>
<main class='welcome-body'>
  <p class='welcome-text'>
    This page is a work in progress, but this is the perfect place to start if you are looking to see what I am capable of as a software developer thus far!
  </p>
  <section class='welcome-picture'>
    <img src={Pic} alt="example"/>
  </section>
  <a href={Resume} class='direct-link'>View my Resume</a>
  <button class='download-button'>
    <a href={Resume} class='direct-link' download>
      Download my Resume
    </a>
  </button>
</main>
<footer class='footer-link-container'>
  <p class='footer-text'>Direct Project Links:</p>
  <a href={projects['Avian Anthems']} class='footer-link'>Avian Anthems</a>
  <a href={projects['Mars Chronicles']} class='footer-link'>Mars Chronicles</a>
  <a href={projects['Hyper Loom']} class='footer-link'>Hyper Loom</a>
</footer>

<style>
  h1 {
    display:flex;
    justify-content: center;
    font-size: 4rem;
  }
  p {
    display:flex;
    justify-content: center;
    font-size: 2rem;
  }
  section {
    display: flex;
    justify-content: center;
  }
  img {
    max-height: 60vh;
    max-width: 60vw;
    border-radius: 1rem;
    border: 1px solid black;
  }
  footer {
    display: flex;
    align-items: center;
    flex-direction: column;
    font-size: 1.5rem;
  }
</style>