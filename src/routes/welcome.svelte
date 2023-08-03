<script>
  import Resume from '$lib/assets/ShaneMisraATS.pdf'
	import Pic from '$lib/assets/Shane_Profile.jpg'
</script>

<main class='welcome-body'>
  <section class='left-panel'>

  </section>
  <p class='welcome-text'>
    This page is a work in progress, but this is the perfect place to start if you are looking to see what I am capable of as a software developer thus far!
  </p>
  <div class='resume-container'>
    <section class='welcome-picture'>
      <img src={Pic} alt="the website creator, Shane Misra"/>
    </section>
    <button class='resume-button view-button'>
      <a href={Resume} class='direct-link'>View my Resume</a>
    </button>
    <button class='resume-button download-button'>
      <a href={Resume} class='direct-link' download>Download my Resume</a>
    </button>
  </div>
  </main>

  <style>
  
  .welcome-body {
    display:flex;
    background: rgba(240, 248, 255, 0.426);
  }

  p {
    display:flex;
    justify-content: center;
    font-size: 2rem;
  }
  .resume-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: .1rem;
    padding: .15rem;
    border: 1px solid black;
  }
  .welcome-picture {
    display: flex;
    justify-content: center;
  }
  .resume-button {
    scale: 1.1;
    border-radius: .25rem;
    background-color: rgba(102, 51, 153, 0.535);
  }

  .resume-button:hover {
    animation: grow-and-shrink infinite 2s;
  }

  .direct-link {
    border: 1px solid black;
  }
  img {
    max-height: 60vh;
    max-width: 60vw;
    border-radius: 1rem;
    border: 1px solid black;
  }

  @keyframes grow-and-shrink {
    0% {
      scale: 1.1;
    }
    20% {
      scale: 1.13;
    }
    40% {
      scale: 1.15;
    }
    60% {
      scale: 1.15;
    }
    80% {
      scale: 1.13;
    }
    100% {
      scale: 1.1
    }
  }
  </style>