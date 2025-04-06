<script lang="ts">

let { title } : { title:string } = $props()
</script>



<a href="/pages/Bookings" class="angled-background">
	<span class="link-text">{title}</span>
</a>

<style>
	a {
		background-color: var(--backGround, white);
		padding: var(--padding, 2%);
		border-radius: 10px 100px / 120px;
		text-decoration: none;
		color: white;
		min-width: 95px;
		white-space: nowrap;
		color: var(--text-color, white);
	}
</style>
