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
      width: 100vw;
      height: 100vh;
      background: aliceblue;
      background-image: url('$lib/assets/MirroredTundra.png');
      background-size: cover;
    }

  h1 {
    display:flex;
    justify-content: center;
    font-size: 4rem;
    background: rgba(240, 248, 255, 0.426);
    border-radius: .75rem;
  }

  .header-link-container {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
  
  .footer-text {
    display:flex;
    justify-content: center;
    font-size: 2rem;
  }
  
  footer {
    display: flex;
    align-items: center;
    flex-direction: column;
    font-size: 1.5rem;
  }
  
    :global(a) {
      text-decoration: none;
      color: aliceblue;
    }
  
    :global(a):hover {
      color: rebeccapurple;
    }
</style>