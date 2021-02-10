<script>
	export let initialCounter = 0;
	export let maxCounter = 0;
	let counter = initialCounter;
	const handleClick = () => counter++;
	$: isEvenOrOdd = counter % 2 === 0 ? "Is Even" : "Is Odd";
	$: if (counter > maxCounter) {
		console.log("limit exceeded");
		counter = maxCounter;
	}
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	span {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<button on:click={handleClick}>Increment</button><br />
	<span>[{counter}]</span>
	<span>{isEvenOrOdd}</span>
	<p>
		Visit the
		<a href="https://svelte.dev/tutorial">Svelte tutorial</a>
		to learn how to build Svelte apps.
	</p>
</main>
