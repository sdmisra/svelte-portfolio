<script>
	import Pic from '$lib/assets/Shane_Profile.jpg'
  let projects = {
    'Avian Anthems' : 'https://avian-anthems.vercel.app/',
    'Mars Chronicles' : 'https://mars-chronicles.vercel.app/',
    'Hyper Loom' : 'https://hyper-loom-explorer.vercel.app/'
  }
</script>

<h1>Welcome to my Professional Portfolio!</h1>
<p>
  This page is a work in progress, but this is the perfect place to start if you are looking to see what I am capable of as a software developer thus far!
</p>
<div>
  <img src={Pic} alt="example"/>
</div>
<footer>
  <p>Showcase:</p>
  <a href={projects['Avian Anthems']}>Avian Anthems</a>
  <a href={projects['Mars Chronicles']}>Mars Chronicles</a>
  <a href={projects['Hyper Loom']}>Hyper Loom</a>
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
  div {
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