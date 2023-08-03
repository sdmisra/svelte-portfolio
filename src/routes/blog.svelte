<script>
  import {onMount} from 'svelte'
  import {getHeadlines, getSearch} from '$lib/apiCalls.js'
  let displayedStories = []
  let searchText = ''

  onMount(async ()=> {
    let headlines =  await getHeadlines()
    displayedStories = headlines.articles
  })

  const searchFunction = async (query)=> {
    let results = await getSearch(query)
    displayedStories = results.articles
  }

</script>

<main class='blog-body'>
  <div class="search-bar">
    <input type='text' class="input-bar" placeholder="Search for a story..." on:change={event => searchText = event.target.value} 
    value={searchText}/>
    <button class="search-button" 
    on:click={searchFunction(searchText) }>Search</button>
  </div>
  <section class="story-container">
    {#each displayedStories as story}
    <section class='story-card'>
      <img src={story.urlToImage} alt={story.title} class='thumbnail'/>
      <span class='story-title'>{story.title}</span>
      <span>Date: {story.publishedAt.slice(0,10)}</span>
      <a href={story.url}>Link to full story</a>
      </section>
    {:else}
      <p class='loading-text'>Loading Articles!</p>
    {/each}
  </section>
</main>

<style>

  .loading-text {
    font-family: 'Menzanine', sans-serif;
    color: aliceblue;
    text-shadow: -1px 1px 2px #000,
				  1px 1px 2px #000,
				  1px -1px 0 #000,
				  -1px -1px 0 #000;
  }
  .story-card {
    display:flex;
    flex-direction: column;
    align-items: center;
    margin: .15rem;
    padding: .15rem;
    background: rgba(153, 183, 214, 0.504);
    border: 1px black solid;
    width: 48%;
  }
  .story-container {
    display:flex;
    flex-wrap: wrap;
    width: 90vw;
  }
  .thumbnail {
    border: 1px aliceblue solid;
    border-radius: .2rem;
    width: 45%;
    height: 40%;
  }
  .blog-body {
    display:flex;
    flex-direction: column;
    align-items: center;
    min-height: 60vh;
    min-width: 100%;
    background: rgba(240, 248, 255, 0.522);
    border: 2px rgba(240, 248, 255, 0.5) solid;
    border-radius: .25rem;
    margin: .15rem;
  }
</style>