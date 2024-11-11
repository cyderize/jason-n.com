<script>
	import Fa from 'svelte-fa';

	/**
	 * @type {string}
	 */
	export let href;

	/**
	 * @type {import("@fortawesome/fontawesome-common-types").IconDefinition}
	 */
	export let icon;

	/**
	 * @type {string}
	 */
	export let variant = 'normal';
</script>

<a class="button-link" class:is-primary={variant === 'primary'} {href}>
	<span class="icon"><Fa {icon} /></span>
	<span><slot /></span>
</a>

<style>
	.button-link::before {
		content: unset;
	}
	.button-link {
		border-radius: 0.5rem;
		padding: 0.5rem 0.8rem;
		display: inline-flex;
		gap: 0.5rem;
		background-color: #00000027;
		transition: background-color 0.2s ease;
		color: inherit;
	}
	.button-link:hover {
		background-color: #00000044;
	}
	.button-link.is-primary {
		background-color: #007ee6;
		color: #fff;
	}

	.button-link.is-primary:hover {
		background-color: #135ec0;
	}
</style>
