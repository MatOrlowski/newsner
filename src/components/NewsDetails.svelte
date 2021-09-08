<script>
	import Card from '../shared/Card.svelte'
	export let news;
</script>

<Card source={news.urlToImage}>
	<h3><a href={news.url}>{news.title}</a></h3>
	<p>{news.source.name}</p>
</Card>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap');

  h3{
    font-family: 'Ubuntu', sans-serif;
  }
</style>
