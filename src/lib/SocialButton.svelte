<script>
	import Fa from 'svelte-fa';

	/**
	 * @type {import("@fortawesome/fontawesome-common-types").IconDefinition}
	 */
	export let icon;

	/**
	 * @type {string}
	 */
	export let name;

	/**
	 * @type {string}
	 */
	export let href;
</script>

<a class="social-button" title={name} {href}>
	<Fa {icon} />
</a>

<style>
	.social-button::before {
		content: unset;
	}
	.social-button {
		padding: 0.2rem;
		opacity: 0.85;
		transition: opacity 0.2s ease;
	}

	.social-button:hover {
		opacity: 1;
	}
</style>
