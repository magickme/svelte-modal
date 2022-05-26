<script>
	import Header from '$lib/header/Header.svelte';
	import {isOverlayOpen} from "../stores/OverlayStore.js";
	import Overlay from "../components/Overlay.svelte";
	import '../app.css';
</script>

<Header />

{#if $isOverlayOpen}
	<Overlay>
		<p class="text-white text-4xl">They played us like a <span class="text-red">damn fiddle</span>!</p>
	</Overlay>
{/if}
<main>
	<slot />
</main>

<footer>
	<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
