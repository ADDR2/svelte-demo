<script>
	import Description from './components/Description.svelte';
	export let name = 'something';

	let numbers = [1, 2, 3, 4];

	$: console.log(numbers);
</script>

<main>
	<h1 class={'lol'}>Hello {name.toLowerCase()}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>

	<Description numbers={numbers} {...{ ja: 3 }}/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		font-size: 4em;
		font-weight: 100;
	}

	p {
		color: blue;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>