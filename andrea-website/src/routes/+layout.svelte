<script lang="ts">
	import TopNavBar from '$lib/components/topNavBar.svelte';
	let { children } = $props();

	let navLinks = {
		links: ['Home', 'About', 'Other']
	};
</script>

<section>
	<div>
		<TopNavBar title={'Kinesiology with Andrea'} {navLinks} />
	</div>
	<div class="pages">
		{@render children()}
	</div>
	<div class="footer"></div>
</section>

<style>
	:global(html, body) {
		height: 100%;
		margin: 0;
	}

	.pages {
		min-height: 100vh;
		max-width: 100%;
		/* background: linear-gradient(to right, var(--main-color-green), white); */
	}
</style>
