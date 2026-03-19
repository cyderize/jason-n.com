<script>
	import Fa from 'svelte-fa';

	/**
	 * @typedef {Object} Props
	 * @property {import("@fortawesome/fontawesome-common-types").IconDefinition} icon
	 * @property {string} name
	 * @property {string} href
	 */

	/** @type {Props} */
	let { icon, name, href } = $props();
</script>

<a class="social-button" title={name} {href} rel="external">
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
