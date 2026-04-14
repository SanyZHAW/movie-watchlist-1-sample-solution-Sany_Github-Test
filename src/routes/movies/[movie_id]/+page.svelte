<script>
  let { data } = $props();
</script>

<a href="/movies">Back</a>

<h1>{data.movie.title}</h1>

<img src={data.movie.poster} alt={data.movie.title} width="250" />

<p>Jahr: {data.movie.year}</p>
<p>Dauer: {data.movie.length}</p>

<h3>Cast:</h3>
<ul>
  {#each data.movie.actors as actor}
    <li>{actor}</li>
  {/each}
</ul>

<form method="POST" action="?/delete">
	<input type="hidden" name="id" value={data.movie._id} />
	<button type="submit">Delete Movie</button>
</form>

