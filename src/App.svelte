<script>
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
	import NewsList from './components/NewsList.svelte';
</script>

<Header />
<main>
	<NewsList />
</main>
<Footer />

<style>
	/* main {
		display: grid;
		align-items: center;
		justify-content: center;
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	} */

	/* h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	} */

	/* @media (min-width: 640px) {
		main {
			max-width: none;
		}
	} */
</style>
