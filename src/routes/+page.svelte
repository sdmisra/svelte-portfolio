<script>
  import { Router, Route, Link } from "svelte-routing";
  import Resume from '$lib/assets/ShaneMisraATS.pdf'
	import Pic from '$lib/assets/Shane_Profile.jpg'
  import Background from '$lib/assets/loom_background.jpg'

  import Blog from './blog.svelte'
  import Projects from './projects.svelte'
  import AboutMe from './aboutme.svelte'

  let projects = {
    'Avian Anthems' : 'https://avian-anthems.vercel.app/',
    'Mars Chronicles' : 'https://mars-chronicles.vercel.app/',
    'Hyper Loom' : 'https://hyper-loom-explorer.vercel.app/'
  }
export let url ='';
</script>

<Router {url}>
<header class='portfolio-header'>
  <h1 class='header-text'>Welcome to my Professional Portfolio!</h1>
  <Link to='/'>Home</Link>
  <nav class='header-link-container'>
    <Link to='/projects'> Projects </Link>
    <Link to='/about'> About Me </Link>
    <Link to='/blog' >Blog </Link>
  </nav>
</header>
<Route exact path='/'>
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
</Route>
<Route exact path='/about'>
  <AboutMe />
</Route>
<Route exact path='/blog'>
  <Blog />
</Route>
<Route exact path='/projects'>
  <Projects />
</Route>
</Router>
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
    background: radial-gradient(circle, rgba(232,208,65,0.94) 5%, rgba(227,187,80,0.91) 25%, rgba(186,27,194,1) 100%);
    border-radius: .75rem;
  }
  .header-link-container {
    display: flex;
    flex-direction: column;
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