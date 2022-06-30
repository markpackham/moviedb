<script>
	let inputValue = '';
	let active = false;
</script>

<form class="search">
	<label for="search_movie">Search Movie</label>
	<input on:focus={() => (active = true)} bind:value={inputValue} name="search_movie" type="text" />
	<button type="submit">Search</button>
</form>

<style>
	button {
		font-size: 0.7rem;
		padding: 0rem 1rem;
		background: rgb(96, 110, 201);
		color: white;
		font-weight: bold;
		border: none;
		position: absolute;
		bottom: 50%;
		right: 0;
		transform: translate(0, 50%);
		height: 100%;
		border-top-right-radius: 10px;
		border-bottom-right-radius: 10px;
		cursor: pointer;
	}

	input {
		width: 100%;
		border: none;
		font-size: 1rem;
		outline: none;
		color: rgb(255, 255, 255);
		padding: 0.5rem 0.1rem;
		transition: background 0.75s ease-out;
		font-weight: bold;
		background: rgb(63, 63, 63);
		border-radius: 10px;
		padding: 1rem;
	}

	label {
		position: absolute;
		font-size: 0.8rem;
		top: 50%;
		left: 0;
		transform: translate(0, -50%);
		pointer-events: none;
		color: white;
		padding: 0rem 1rem;
	}

	.search {
		position: relative;
		width: 30%;
		margin: 1rem;
	}
</style>
