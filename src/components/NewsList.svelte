<script>
	import NewsDetails from './NewsDetails.svelte';
	import { onMount } from 'svelte';

	let newsTable = [];
	onMount(async () => {
		const res = await fetch(
			`https://newsapi.org/v2/top-headlines?country=pl&apiKey=9c6e4339eda04a3e961469a00a816e2d`
		);
		let data = await res.json();
		newsTable = data.articles;
	});
</script>

<div class="news-list">
	{#each newsTable as news}
		<NewsDetails {news}/>
	{/each}
</div>

<style>
  .news-list{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 20px;
		align-items: center;
		justify-content: center;
		text-align: center;
		padding: 1em;
		margin: 0 auto;
  }
</style>
