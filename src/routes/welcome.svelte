<script>
  import Resume from '$lib/assets/ShaneMisraATS.pdf'
	import Pic from '$lib/assets/Shane_Profile.jpg'
  import Background from '$lib/assets/loom_background.jpg'
</script>

<main class='welcome-body'>
  <p class='welcome-text'>
    This page is a work in progress, but this is the perfect place to start if you are looking to see what I am capable of as a software developer thus far!
  </p>
  <section class='welcome-picture'>
    <img src={Pic} alt="the website creator, Shane Misra"/>
    <img src={Background} alt='background'/>
  </section>
  <a href={Resume} class='direct-link'>View my Resume</a>
  <button class='download-button'>
    <a href={Resume} class='direct-link' download>
      Download my Resume
    </a>
  </button>
  </main>

  <style>

  p {
    display:flex;
    justify-content: center;
    font-size: 2rem;
  }
  .welcome-picture {
    display: flex;
    justify-content: center;
  }
  img {
    max-height: 60vh;
    max-width: 60vw;
    border-radius: 1rem;
    border: 1px solid black;
  }
  </style>