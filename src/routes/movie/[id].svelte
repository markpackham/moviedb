<script context="module">
	export async function load({ fetch, params }) {
		const res = await fetch(
			`https://api.themoviedb.org/3/movie/${params.id}?api_key=d5c35e51c81488b19da7c1f572507a3d&language=en-US`
		);

		const movieDetail = await res.json();
		if (res.ok) {
			return {
				props: { movieDetail }
			};
		}
	}
</script>

<script>
	export let movieDetail;
</script>

<div class="movie-details">
	<div class="img-container">
		<img
			src={'https://image.tmdb.org/t/p/original' + movieDetail.backdrop_path}
			alt={movieDetail.title}
		/>
	</div>
	<div class="text-container">
		<h1>{movieDetail.title}</h1>
	</div>
</div>
