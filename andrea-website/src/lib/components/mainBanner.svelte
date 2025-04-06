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
			and limiting beliefs that are holding you back from the life you truly want.
		</p>
		<!-- Reducing stress
		is a powerful first step toward improving your physical and mental wellbeing. Together, we’ll
		explore where you are, where you want to go, and how to get there — empowering you to reach
		your full potential and find lasting peace. -->
		<div class="booking">
			<BookNowButton --padding="10%" title={'Book a consultation'} --backGround="#7dbb8e" />
		</div>
	</div>

	<div class="title-container"></div>
</section>

<style>

	
	* {
		font-family: 'Prata', serif;
	}

	.booking {
		margin-bottom: 4%;
	}

	.image-container img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		display: block;
		border-radius: 0 16px 16px 0;
	}
	section {
		padding-top: 2.5%;
		height: 600px;
		width: 100vw;
		display: grid;
		grid-template-columns: repeat(6, 1fr);
		grid-template-rows: repeat(6, 1fr);
		background: linear-gradient(to bottom, var(--main-color-green) 0%, white 40%);
	}

	.image-container {
		/* Grid positioning */
		grid-row-start: 1;
		grid-row-end: 6;
		grid-column-start: 1;
		grid-column-end: 4;
	}

	.text-container {
		grid-column-start: 4;
		grid-column-end: 7;
		grid-row-start: 2;
		grid-row-end: 3;

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
		margin-top: 4%;
	}

	h1 {
		font-size: var(--title-font);
		max-width: 80%;
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
		max-width: 80%;
		letter-spacing: 0.5px;
		word-wrap: break-word;
		text-indent: 50px;
	}

	@media (max-width: 915px) {
	section {
		display: flex;
		flex-direction: column;
		padding: 5% 2%;
		height: auto; /* important */
	}

	.image-container {
		width: 100%;
		margin: 0 auto 2rem auto;
		grid-row: unset;
		grid-column: unset;
	}

	.text-container {
		width: 100%;
		margin: 0 auto;
		border-radius: unset;
		grid-column: unset;
		grid-row: unset;
		box-shadow: none;
		padding: unset;
	}

	h1 {
		font-size: 22px;
	}

	p {
		font-size: 16px;
		text-indent: 0;
	}
	}
</style>
