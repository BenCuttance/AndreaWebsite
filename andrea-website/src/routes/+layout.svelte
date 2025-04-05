<script lang="ts">
	import TopNavBar from '$lib/components/topNavBar.svelte';

	let navLinks = {
		links: ['Home', 'About', 'Other']
	};
</script>

<section>
	<TopNavBar title={'Kinesiology with Andrea'} {navLinks} />
</section>

<style>
</style>
