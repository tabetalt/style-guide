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
			<section id="sub-menu">
				<b> Sub-menu </b>
				<a href="/"> Home </a>
				<a href="/"> About </a>
				<a href="/"> Contact </a>
			</section>
			<section id="legal">
				<b> Legal </b>
				<a href="/"> Privacy </a>
				<a href="/"> Terms </a>
				<a href="/"> Cookies </a>
			</section>
			<section id="find-us">
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
