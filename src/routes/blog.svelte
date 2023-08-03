<script>
  import {onMount} from 'svelte'
  import {getHeadlines, getSearch} from '$lib/apiCalls.js'
  let headlineStories = []
  let resultsStories = []
  let searchText = ''

  onMount(async ()=> {
    let headlines =  await getHeadlines()
    headlineStories = headlines.articles
  })

  const searchFunction = async (query)=> {
    let results = await getSearch(query)
    resultsStories = results.articles
  }

</script>

<main class='blog-body'>
  <div class="search-bar">
    <input type='text' class="input-bar" placeholder="Search for a story..." on:change={event => searchText = event.target.value} 
    value={searchText}/>
    <button class="search-button" 
    on:click={searchFunction(searchText) }>Search</button>
  </div>
  <section class="headlines">
    {#each headlineStories as story}
      <figure class='story-card'>
        <img src={story.urlToImage} alt={story.title} class='thumbnail'/>
        <figcaption>{story.title}</figcaption>
      </figure>
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
    border: 1px black solid;
  }
  .thumbnail {
    max-width: 15%;
    max-height: 10%;
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