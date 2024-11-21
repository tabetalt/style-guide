<script>
	import Buttons from './_components/buttons.svelte';
	import Texts from './_components/texts.svelte';
</script>

<div class="container">
	<section>
		<Texts />
	</section>
	<section>
		<Buttons />
	</section>
</div>

<style>
	section {
		width: 100%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: flex-start;
		gap: 4em;
	}
</style>
