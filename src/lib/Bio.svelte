<script>
	import Portrait from '$lib/img/jason_nguyen.jpg';
	import SocialButton from '$lib/SocialButton.svelte';
	import { faHome, faEnvelope } from '@fortawesome/free-solid-svg-icons';
	import { faGithub } from '@fortawesome/free-brands-svg-icons';
</script>

<div class="wrapper">
	<div class="bio">
		<img class="portrait" src={Portrait} alt="Jason Nguyen" />
		<h3>Jason Nguyen</h3>
		<div>Software developer</div>
		<div class="socials">
			<SocialButton href="/" name="Website" icon={faHome} />
			<SocialButton href="mailto:hello@jason-n.com" name="E-mail" icon={faEnvelope} />
			<SocialButton href="https://github.com/cyderize" name="GitHub" icon={faGithub} />
		</div>
	</div>
</div>

<style>
	.wrapper {
		padding: 2rem;
	}

	.bio {
		padding: 4rem 1rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: #a8bfd11a;
	}

	.portrait {
		width: 200px;
		height: 200px;
		border-radius: 50%;
		object-fit: cover;
	}

    .socials {
        padding-top: 1rem;
    }

	@media (max-width: 960px) {
		.wrapper {
			padding: 0;
		}
	}
</style>
