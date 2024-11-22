<script>
	import logo from './logo.svg';
	import darkLogo from './dark-logo.svg';
	const title = 'Style guide';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<main>
	<header>
		<img src={logo} alt="Tabetalt logo" />
		<section id="menu">
			<button class="ghost"> Menu </button>
		</section>
	</header>
	<section class="container">
		<slot></slot>
	</section>
	<footer>
		<img src={darkLogo} alt="Tabetalt logo" />
		<div class="link-menu">
			<section id="sub-menu" class="footer-menu">
				<b> Sub-menu </b>
				<a href="/"> Home </a>
				<a href="/"> About </a>
				<a href="/"> Contact </a>
			</section>
			<section id="legal" class="footer-menu">
				<b> Legal </b>
				<a href="/"> Privacy </a>
				<a href="/"> Terms </a>
				<a href="/"> Cookies </a>
			</section>
			<section id="find-us" class="footer-menu">
				<b> Find us </b>
				<a href="/"> Facebook </a>
				<a href="/"> Instagram </a>
				<a href="/"> Twitter </a>
			</section>
		</div>
	</footer>
</main>

<style scoped>
	header {
		display: grid;
		grid-template-columns: 1fr 3fr;
		align-items: center;
		padding: 1em;
		background-color: var(--header-background);
		min-height: 100px;
		button {
			width: fit-content;
			padding: 1em;
		}
		section {
			display: flex;
			justify-content: flex-end;
		}
		img {
			justify-self: center;
		}
	}
	img {
		width: clamp(50px, 50%, 300px);
	}
	footer {
		background-color: var(--footer-background);
		color: var(--light-color);
		min-height: 100px;
		padding: 1em;
		display: grid;
		grid-template-columns: 1fr 3fr;
		justify-content: center;
		img {
			justify-self: center;
		}
	}
	.link-menu {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
	}
	.footer-menu {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 1em;
	}
</style>
