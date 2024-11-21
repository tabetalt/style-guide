<script>
	import logo from './logo.svg';
	const title = 'Style guide';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<main>
	<header>
		<img src={logo} alt="Svelte logo" />
		<section id="menu">
			<button class="ghost">
				Menu
			</button>
		</section>
	</header>
	<section class="container">
		<slot></slot>
	</section>
	<footer>
	</footer>
</main>

<style scoped>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1em;
		background-color: var(--header-background);
		min-height: 100px;
		button {
			padding: 1em;
		}
	}
	img {
		width: clamp(50px, 50%, 300px);
	}
	footer {
		display: flex;
		justify-content: center;
		flex-direction: row;
		padding: 1em;
		background-color: var(--footer-background);
		min-height: 100px;
	}
</style>
