<script>
  import Resume from '$lib/assets/ShaneMisraATS.pdf'
	import Pic from '$lib/assets/Shane_Profile.jpg'
</script>

<main class='welcome-body'>
  <section class='left-panel'>
    <p class='welcome-text'>
      This page is a work in progress, but this is the perfect place to start if you are looking to see what I am capable of as a software developer thus far!
    </p>
  </section>
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
  .left-panel {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
  }
  p {
    font-size: 2rem;
  }

  .resume-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: .2rem;
    padding: .35rem;
  }
  .welcome-picture {
    display: flex;
    justify-content: center;
  }
  .resume-button {
    margin: .1rem;
    padding: .2rem;
    border-radius: .25rem;
    background-color: rgba(102, 51, 153, 0.45);
  }

  .resume-button:hover {
    animation: grow-and-shrink linear infinite 3.5s;
  }

  /* .direct-link {
  } */
  img {
    max-height: 60vh;
    max-width: 60vw;
    border-radius: 1rem;
    border: 1px solid black;
  }

  @keyframes grow-and-shrink {
    0% {
      scale: 1;
      background-color: rgba(102, 51, 153, 0.35);
    }
    10% {
      scale: 1.04;
      background-color: rgba(102, 51, 153, 0.35);
    }
    20% {
      scale: 1.08;
      background-color: rgba(102, 51, 153, 0.45);
    }
    30% {
      scale: 1.12;
      background-color: rgba(102, 51, 153, 0.55);
    }
    40% {
      scale: 1.16;
      background-color: rgba(102, 51, 153, 0.65);
    }
    50% {
      scale: 1.20;
      background-color: rgba(102, 51, 153, 0.75);
    }
    60% {
      scale: 1.16;
      background-color: rgba(102, 51, 153, 0.65);
    }
    70% {
      scale: 1.12;
      background-color: rgba(102, 51, 153, 0.55);
    }
    80% {
      scale: 1.08;
      background-color: rgba(102, 51, 153, 0.45);
    }
    90% {
      scale: 1.04;
      background-color: rgba(102, 51, 153, 0.45);
    }
    100% {
      scale: 1;
      background-color: rgba(102, 51, 153, 0.35);
    }
  }
  </style>