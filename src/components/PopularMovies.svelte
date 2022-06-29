<script>
	export let popular;
</script>

<h3>Popular Movies</h3>
<div class="popular-movies">
	{#each popular as movie}
		<h4>{movie.title}</h4>
	{/each}
</div>
