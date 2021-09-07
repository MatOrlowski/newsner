<script>
	export let source;
</script>

<div class="card">
	<img src={source} class="card-img-top" alt="..." />
	<div class="card-body">
		<slot />
	</div>
</div>

<style>
	.card {
		width: 640px;
		height: fit-content;
		cursor: pointer;
		background: #ededed;
		margin: 20px;
		border-radius: 6px;
		box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
	}
	.card-img-top{
		width: 640px;
		height: 336px;
	}
	.card-body{
		width: 640px;
		height: 200px;
	}
</style>
