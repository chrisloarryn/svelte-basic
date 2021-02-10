<script>
	import Counter from './Counter.svelte'
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	span {
		color: #09f;
	}
</style>

<Counter initialCounter={2}/>
<Counter initialCounter={10}/>
<Counter />
<main>
	<span>We've spans</span>
</main>