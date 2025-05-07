<script lang="ts">
	import { page } from '$app/state';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
	import Fa from 'svelte-fa'
	import { faBars, faXmark } from '@fortawesome/free-solid-svg-icons'
	import { faSquareFacebook} from '@fortawesome/free-brands-svg-icons';
	import { slide } from 'svelte/transition';

	let sidebar = $state(false);

	function toggleSidebar() {
		sidebar = !sidebar;
	}

	let container = $state();
	function onWindowClick(e) {
		console.log(e.target)
		if (container.contains(e.target) === false) {
			// sidebar = false;
		}
	}
</script>

<svelte:window onclick={onWindowClick} />

<header class="sticky top-0 bg-[#f3e9dd]">
	<div
		class="m-4"
		bind:this={container}
	>
		<button class="text-2xl" onclick={toggleSidebar}>
			<Fa icon={faBars} size="2x"  />
		</button>
		{#if sidebar}
			<aside
				class="absolute top-0 left-0 w-64 h-screen bg-[#fffdf9] p-6 shadow-md z-40 transition-transform duration-300"
				transition:slide={{duration: 300, axis: "x"}}
			>
				<div class="flex justify-between items-center m-4">
					<h2 class="text-2xl font-semibold text-[#a1886e]">Seeblick</h2>
					<button class="text-xl" onclick={toggleSidebar}>
						<Fa icon={faXmark} size="lg"  />
					</button>
				</div>


				<div class="m-4">
					<a class="block px-4 py-2 rounded hover:bg-[#f3e9dd] whitespace-nowrap "
						 href="./"
						 onclick={toggleSidebar}
					>
						🏠 Start
					</a>
					<a class="block px-4 py-2 rounded hover:bg-[#f3e9dd] whitespace-nowrap "
						 href="./Speisekarte"
						 onclick={toggleSidebar}
					>
						🍽️ Speisekarte
					</a>
					<a class="block px-4 py-2 rounded hover:bg-[#f3e9dd] whitespace-nowrap" href="./Restaurant"
						 onclick={toggleSidebar}
					>
						🏡 Restaurant
					</a>
					<a class="block px-4 py-2 rounded hover:bg-[#f3e9dd] whitespace-nowrap "
						 href="./Übernachtung"
						 onclick={toggleSidebar}
					>
						🛏️ Übernachtung
					</a>
					<a class="block px-4 py-2 rounded hover:bg-[#f3e9dd] whitespace-nowrap " href="./Kontakt"
						 onclick={toggleSidebar}
					>
						📍 Kontakt
					</a>
					<a class="block px-4 py-2 rounded hover:bg-[#f3e9dd] whitespace-nowrap" href="./Impressum"
						 onclick={toggleSidebar}
					>
						📝 Impressum
					</a>
				</div>
			</aside>
		{/if}

	</div>

	<div class="m-4">
		<a href="https://www.facebook.com/traditonshausseeblick/" target="_blank" class="text-[#a1886e] text-lg">
			<Fa icon={faSquareFacebook}  size="2x" primaryColor="#1877F2"/>
		</a>
	</div>
</header>


<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
