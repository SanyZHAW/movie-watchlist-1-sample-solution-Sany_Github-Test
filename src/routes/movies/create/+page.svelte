<script>
  let { form } = $props();
</script>

<a href="/movies">Back</a>

<h1>Add Movie</h1>

<form method="POST" action="?/create">
  <div>
    <label>Title</label>
    <input name="title" type="text" />
  </div>

  <div>
    <label>Year</label>
    <input name="year" type="number" />
  </div>

  <div>
    <label>Length</label>
    <input name="length" type="text" placeholder="120 Minuten" />
  </div>

  <button type="submit">Add Movie</button>
</form>

{#if form?.success}
  <p>Movie created!</p>
{/if}
