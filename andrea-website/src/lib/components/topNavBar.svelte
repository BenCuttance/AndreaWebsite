<script lang="ts">
	import BookNowButton from './bookNowButton.svelte';
	import '../../styles/global.css';

	let { title, navLinks }: { title: string; navLinks: { links: string[] } } = $props();

	let activeLink = $state('Home');

	let changeActiveLink = (link: string) => {
		activeLink = link;
	};
</script>

<section>
	<div class="title">
		{title}
	</div>
	<div class="links">
		{#each navLinks.links as link}
			<a
				href="/pages/{link}"
				class={activeLink === link ? 'active' : ''}
				onclick={() => changeActiveLink(link)}>{link}</a
			>
		{/each}
		<BookNowButton title={'Book now'} --text-color='#7dbb8e'/>
	</div>
</section>

<style>
	* {
		font-family: 'Prata', serif;
	}

	.active {
		text-decoration: underline;
		text-decoration-thickness: 1px; /* Thin the line */
		text-underline-offset: 4px; /* Adjust the distance between the word and the line */
	}

	section {
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		/* grid-template-columns: repeat(4, 1fr); */
		padding: 2%;
		align-items: center;
		background-color: var(--main-color-green);
	}

	.title {

		display: flex;
		font-size: 45px;
		color: white;
		display: flex;
		justify-content: space-around;
		white-space: nowrap;
		text-align: center;
	}

	.links {
		font-size: 20px;
		grid-column-start: 4;
		display: flex;
		justify-content: space-around;
		align-items: center;
		gap: 10%;
	}

	a {
		text-decoration: none;
		color: white;
	}

	a:active {
		text-decoration: underline;
	}

	@media (max-width: 1100px){
		section{
			flex-direction: column;
			align-items: stretch;
		}
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

		.title {
			white-space: pre-wrap;
		}
	@media (max-width: 450px){
		.links{
			flex-direction: column;
		}
	}
	}
</style>
