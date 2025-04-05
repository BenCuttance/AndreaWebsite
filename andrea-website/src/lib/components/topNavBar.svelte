<script lang="ts">
	import BookNowButton from './bookNowButton.svelte';
	import '../../styles/global.css';

	let { title, navLinks }: { title: string; navLinks: { links: string[] } } = $props();
</script>

<section>
	<div class="title">
		{title}
	</div>
	<div class="links">
		{#each navLinks.links as link}
			<a href={link}>{link}</a>
		{/each}
		<BookNowButton />
	</div>
</section>

<style>
	* {
		font-family: 'Lato', sans-serif;
	}

	section {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		padding: 2%;
		align-items: center;
	}

	.title {
		display: flex;
		font-size: 35px;
		color: var(--main-color-green);
		display: flex;
		justify-content: space-around;
		white-space: nowrap;
	}

	.links {
		font-size: 20px;
		grid-column-start: 4;
		display: flex;
		justify-content: space-around;
		align-items: center;
		gap: 2%;
	}

	a {
		text-decoration: none;
		color: var(--main-color-green);
	}

	@media (max-width: 685px) {
		section {
			grid-template-columns: unset;
			grid-template-rows: repeat(2, 1fr);
		}

		.links {
			grid-column-start: unset;
			grid-row-start: 2;
		}
	}
</style>
