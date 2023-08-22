<script>
  import Resume from '$lib/assets/ShaneMisra - ATS Version.pdf'
	import Pic from '$lib/assets/Shane_Profile.jpg'
</script>

<main class='welcome-body'>
  <section class='left-panel'>
    <p class='welcome-text'>
     My name is Shane Misra - I am a software developer with a foundation in FE technologies!
    </p>
    <p class='welcome-text'>
     Please have a look around, and check out a few of my deployed project links below for immediate examples of my work.
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
    background: rgba(240, 248, 255, 0.35);
    border: 2px rgba(240, 248, 255, 0.5) solid;
    border-radius: .25rem;
    margin: .15rem;
  }
  .left-panel {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    margin: .5rem;
    padding: .25rem;
  }
  p {
    font-family: 'Rethogen Atomics', sans-serif;
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
  .welcome-text {
    font-size: 4rem;
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
    box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 1px 3px 1px;
    border: 1px rgba(240, 248, 255, 0.20) solid;
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