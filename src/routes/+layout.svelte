<script>
	import { base } from '$app/paths';
	import logo from './logo.svg';
	import darkLogo from './dark-logo.svg';
	const title = 'Style guide';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<main>
	<header>
		<img src={logo} class="logo" alt="Tabetalt logo" />
		<section id="menu">
			<button class="ghost"> Menu </button>
		</section>
	</header>
	<section class="container">
		<slot></slot>
	</section>
	<footer>
		<img src={darkLogo} class="logo" alt="Tabetalt logo" />
		<div class="link-menu">
			<section id="sub-menu">
				<b> Sub-menu </b>
				<a href="{base}/"> Home </a>
				<a href="{base}/"> About </a>
				<a href="{base}/"> Contact </a>
			</section>
			<section id="legal">
				<b> Legal </b>
				<a href="{base}/"> Privacy </a>
				<a href="{base}/"> Terms </a>
				<a href="{base}/"> Cookies </a>
			</section>
			<section id="find-us">
				<b> Find us </b>
				<a href="{base}/"> Facebook </a>
				<a href="{base}/"> Instagram </a>
				<a href="{base}/"> Twitter </a>
			</section>
		</div>
	</footer>
</main>

<style scoped>
	header {
		section {
			display: flex;
			justify-content: flex-end;
		}
		img {
			justify-self: center;
		}
	}
	footer {
		img {
			justify-self: center;
		}
	}
	.link-menu {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		section {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			gap: 1em;
		}
	}
</style>
