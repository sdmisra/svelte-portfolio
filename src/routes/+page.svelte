<script>
  import { Router, Route, Link } from "svelte-routing";
  import Blog from './blog.svelte'
  import Projects from './projects.svelte'
  import AboutMe from './aboutme.svelte'
  import Welcome from './welcome.svelte'

  let deployedProjects = {
    'Avian Anthems' : 'https://avian-anthems.vercel.app/',
    'Mars Chronicles' : 'https://mars-chronicles.vercel.app/',
    'Hyper Loom' : 'https://hyper-loom-explorer.vercel.app/'
  }


  export let url ='';
</script>

<Router {url}>
  <header class='portfolio-header'>
    <h1 class='header-text'>Welcome to my Professional Portfolio!</h1>
    <nav class='header-link-container'>
      <Link to='/' class='header-link'>Home</Link>
      <Link to='/projects' class='header-link'> Projects </Link>
      <Link to='/about' class='header-link'> About Me </Link>
      <Link to='/blog' class='header-link'>Blog </Link>
    </nav>
  </header>
  <Route exact path='/'>
    <Welcome />
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
    <p class='footer-text'>A few deployed projects:</p>
    <a href={deployedProjects['Avian Anthems']} class='footer-link'>Avian Anthems</a>
    <a href={deployedProjects['Mars Chronicles']} class='footer-link'>Mars Chronicles</a>
    <a href={deployedProjects['Hyper Loom']} class='footer-link'>Hyper Loom</a>
  </footer>

<style>

  :global(body) {
      margin: 0px;
      width: 100vw;
      height: 100vh;
      background: aliceblue;
      background-image: url('$lib/assets/MirroredTundra.webp');
      background-repeat: no-repeat;
      background-size: cover;
    }

  .header-text {
    text-align: center;
    font-size: 2.5rem;
    font-family: 'Menzanine', sans-serif;
    color: aliceblue;
    text-shadow: -1px 1px 2px #000,
				  1px 1px 2px #000,
				  1px -1px 0 #000,
				  -1px -1px 0 #000;
    background: rgba(240, 248, 255, 0.20);
    border: 2px rgba(240, 248, 255, 0.5) solid;
    border-radius: .75rem;
    margin: .25rem;
  }
  .portfolio-header {
    display:flex;
    flex-direction: column;
    justify-content: center;
  }
  :global(.header-link) {
    margin: .15rem;
    padding: .15rem;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    text-shadow: -1px 1px 2px #000,
				  1px 1px 2px #000,
				  1px -1px 0 #000,
				  -1px -1px 0 #000;
    border-radius:.15rem;
    border: 1px rgba(240, 248, 255, 0.25) solid;
  }
  .header-link-container {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin: .25rem;
    padding: .15rem;
  }
  .footer-link {
    margin: .15rem;
    padding: .15rem;
    background-color: rgba(112, 128, 144, 0.60);
    border: 1px aliceblue solid;
    text-shadow: -1px 1px 2px #000,
				  1px 1px 2px #000,
				  1px -1px 0 #000,
				  -1px -1px 0 #000;
    border-radius: .75rem;
  }
  .footer-link-container {
    margin: .15rem;
    padding: .25rem;
    background: rgba(240, 248, 255, 0.20);
    border: 2px rgba(240, 248, 255, 0.5) solid;
    border-radius: .25rem;
  }
  
  .footer-text {
    display:flex;
    justify-content: center;
    font-size: 2rem;
    background-color: hsla(210, 13%, 50%, 0.90);
    border-radius: .55rem;
    color: aliceblue;
  }
  
  footer {
    display: flex;
    align-items: center;
    flex-direction: column;
    font-size: 1.5rem;
  }
  
    :global(a) {
      font-family: 'Menzanine', sans-serif;
      text-decoration: none;
      color: rgb(233, 229, 239);
    }
  
    :global(a):hover {
      color: aliceblue;
      scale: 1.05;
    }
</style>