<script>
	import Bio from '$lib/Bio.svelte';
	import Landing from '$lib/Landing.svelte';

	let { data } = $props();
</script>

<main>
	<div class="columns">
		<div class="col">
			<Bio />
		</div>
		<div class="col">
			<Landing />
		</div>
	</div>
</main>

<footer>&copy; {data.year} Jason Nguyen</footer>

<style>
	main {
		padding: 1rem 0;
	}

	.columns {
		display: flex;
		gap: 1rem;
		align-items: center;
	}

	.col {
		flex: 1 1 50%;
	}

	@media (max-width: 960px) {
		.columns {
			flex-direction: column;
			align-items: stretch;
		}

		.col {
			padding: 0.5rem;
		}
	}
</style>
