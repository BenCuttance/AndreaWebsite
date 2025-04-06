<script>
	import MainBanner from '$lib/components/mainBanner.svelte';
	import Testimonials from '$lib/components/testimonials.svelte';
</script>

<section>
	<div class="banner">
		<MainBanner />
	</div>
	<div class="seperator">
        <!-- <Testimonials /> -->
	</div>

</section>

<style>

    section{
        display: flex;
        flex-direction: column;
    }
    .seperator{
        margin-top: 2%;
        padding: 2% 0 2% 0;
    }

    @media (max-width:915px){
        
    }

</style>
