<script lang="ts">
	import image from '../images/andreafront.jpg';
	import BookNowButton from './bookNowButton.svelte';
</script>

<section>
	<div class="image-container">
		<img src={image} alt="" />
	</div>
	<div class="text-container">
		<h1>There is more to life — and it's closer than you think.</h1>
		<p>
			If you're feeling that pull for something more, but you're unsure where to begin — you're not
			alone. Join me on a journey to rediscover peace in the present and gently release the blocks
			and limiting beliefs that are holding you back from the life you truly want. Reducing stress
			is a powerful first step toward improving your physical and mental wellbeing. Together, we’ll
			explore where you are, where you want to go, and how to get there — empowering you to reach
			your full potential and find lasting peace.
		</p>
		<div class="booking">
			<BookNowButton --padding="10%" />
		</div>
	</div>

	<div class="title-container"></div>
</section>

<style>
	* {
		font-family: 'Roboto', sans-serif;
	}

	.booking {
		margin-bottom: 4%;
	}

	.image-container img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		display: block;
		border-radius: 16px;
	}
	section {
		height: 600px;
		width: 100vw;
		display: grid;
		grid-template-columns: repeat(6, 1fr);
		grid-template-rows: repeat(6, 1fr);
	}

	.image-container {
		/* Grid positioning */
		grid-row-start: 2;
		grid-row-end: 7;
		grid-column-start: 1;
		grid-column-end: 4;

		margin-left: 2%;
	}

	.text-container {
		grid-column-start: 4;
		grid-column-end: 7;
		grid-row-start: 3;
		grid-row-end: 4;

		background-color: white;
		margin-right: 5%;
		margin-left: -10%; /* overlap into image container */
		margin-top: -2%;
		padding: 2%;
		border-radius: 16px;
		z-index: 2;
		display: flex;
		flex-direction: column;
		align-items: center;
		box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
	}

	h1 {
		font-size: 35px;
		padding: 2%;
		color: #a3b18a;
		text-align: center;
	}

	p {
		font-family: 'Roboto', sans-serif;
		font-size: 1.125rem;
		line-height: 1.6;
		color: #333333;
		text-align: justify;
		margin: 0 0 1.5rem 0;
		max-width: 90%;
		margin-left: auto;
		margin-right: auto;
		letter-spacing: 0.5px;
		word-wrap: break-word;
		text-indent: 50px; /* Optional: Adds a subtle indent for the first line */
	}
</style>
