<script>
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>Powered by <a href="https://nexuspipe.com/?utm_source=ksfrontend" target="_blank" style="color:#ffa820" rel="noreferrer">NexusPIPE</a></p>
	</footer>
</div>

<style lang="scss">
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 16px 16px;
		position: fixed; bottom: 8px; left: 50vw; z-index: 5; transform: translate(-50%,0%);
		background-color: #00000077;
    border-radius: 8px;
		backdrop-filter: blur(16px);
		p {
		margin: 0 0;
		}
	}

	footer a {
		font-weight: bold;
	}

</style>
