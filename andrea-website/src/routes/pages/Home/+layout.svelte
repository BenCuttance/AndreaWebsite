<script>
	import MainBanner from '$lib/components/mainBanner.svelte';
	import Testimonials from '$lib/components/testimonials.svelte';
</script>

<section>
	<div class="banner">
		<MainBanner />
	</div>
	<div class="seperator">
        <Testimonials />
	</div>
    <div class="info">
g
    </div>

</section>

<style>

    section{
        display: flex;
        flex-direction: column;
    }
    .seperator{
        margin-top: .5%;
        margin-bottom: .5%;
    }

    .info{
        background-color: var(--main-color-green);

    }

    @media (max-width:915px){
        
    }

</style>
