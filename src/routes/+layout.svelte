<script lang="ts">
	import Header from './Header.svelte';
	import '../app.css';

	let { children } = $props();
</script>


<div class="flex flex-col min-h-screen">
	<div class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
		<Header />
	</div>

	<main class="flex flex-col flex-1 p-4 w-full max-w-4xl mx-auto box-border overflow-y-auto">
		{@render children()}
	</main>

	<footer class="flex flex-col justify-center items-center p-3 sm:py-3 sm:px-0">
		<p>
			visit <a href="https://svelte.dev/docs/kit" class="font-bold">svelte.dev/docs/kit</a> to learn about SvelteKit
		</p>
	</footer>
</div>
<!--
<div class="app flex-col h-screen overflow-hidden">
	<Header />

	<main class="overflow-y-scroll">
		{@render children()}
	</main>

	<footer>
		<p>
			visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to learn about SvelteKit
		</p>
	</footer>
</div>


<style>
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
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
-->
