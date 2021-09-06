<script>
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
	import SearchBar from './components/SearchBar.svelte';
	import Button from './shared/Button.svelte';
	import Card from './shared/Card.svelte';

	import { onMount } from 'svelte';

	let newsTable = [];
	onMount(async () => {
		const res = await fetch(
			'https://newsapi.org/v2/everything?q=Apple&from=2021-09-06&sortBy=popularity&apiKey=9c6e4339eda04a3e961469a00a816e2d'
		);
		let data = await res.json();
		newsTable = data.articles;
	});
</script>

<Header>
	<SearchBar />
	<Button>SEARCH</Button>
</Header>
<main>
	{#each newsTable as news}
		<Card source={news.urlToImage}>
			<h3><a href={news.url}>{news.title}</a></h3>
			<p>{news.author}</p>
		</Card>
	{/each}
</main>
<Footer />

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 360px;
		margin: 0 auto;
	}

	h1 {
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
