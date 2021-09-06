<script>
	export let source;
</script>

<div class="card" style="width: 18rem;">
	<img src={source} class="card-img-top" alt="..." />
	<div class="card-body">
		<slot />
	</div>
</div>

<style>
	.card {
		width: 360px;
		height: fit-content;
		cursor: pointer;
		background: #ededed;
		margin: 20px;
		border-radius: 6px;
		box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
	}
</style>
