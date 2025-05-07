<script lang="ts">
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="flex relative min-h-screen bg-cover bg-center bg-fixed">
	<main class="flex-1 w-full p-6 animate-fadeIn ">
		<div class="flex flex-col space-y-4">
			<div>
				<section class="bg-white/80 p-6 rounded-lg text-center shadow-md">
					<h1 class="text-3xl font-bold text-[#a1886e]">Willkommen im Traditionshaus Seeblick</h1>
					<p class="mt-2 text-gray-600 text-lg">Genießen Sie unsere Fisch- & Fleischgerichte sowie unvergessliche Übernachtungen auf der Insel Poel.</p>
				</section>
			</div>

			<div class="bg-[#fef6e4] p-6 rounded-lg shadow-md animate-fadeInUp">
				<strong class="text-xl">🏡 Traditionshaus Seeblick</strong>
				<img src="https://www.insel-poel.de/bilder/restaurants/traditionshaus-seeblick-310.jpg" alt="Restaurant Bild" class="w-full my-4 rounded-md" />
				<p>Täglich von 11:00 Uhr – 20:30 Uhr (Küchenschluss um 20:00 Uhr)</p>
				<p>Mittwochs ist Ruhetag</p>
				<p class="mt-2">Tel: 038425 42549</p>
				<p>Email: hallo@traditionshaus-seeblick.de</p>
			</div>

			<div class="bg-[#fef6e4] p-6 rounded-lg shadow-md animate-fadeInUp">
				<strong class="text-xl">🍽️ Restaurant</strong>
				<p class="mt-2">Mit regionalen Speisen und diversen Fischspezialitäten bringen wir Ihnen die Ostsee etwas näher.</p>
				<a href="./Speisekarte" class="inline-block mt-4 text-blue-600 underline">Zur Speisekarte</a>
			</div>

			<div class="bg-[#fef6e4] p-6 rounded-lg shadow-md animate-fadeInUp">
				<strong class="text-xl">🛌 Übernachtung</strong>
				<p class="mt-2">Wachen Sie mit Meeresrauschen auf – unsere charmanten Zimmer und Ferienwohnungen laden zum Träumen ein.</p>
				<a href="./Übernachtung" class="inline-block mt-4 text-blue-600 underline">Mehr erfahren</a>
			</div>

			<div class="bg-[#fef6e4] p-6 rounded-lg shadow-md animate-fadeInUp">
				<strong class="text-xl">🗺️ Lage</strong>
				<p class="mt-2">Einmalige Lage direkt an der Promenade – perfekt für entspannte Spaziergänge am Wasser.</p>
				<p class="mt-2">
					<strong>Adresse:</strong><br>
					Promenade 1<br>
					23999 Ostseebad Insel Poel (OT Am Schwarzen Busch)
				</p>
				<div class="my-4">
					<iframe
						title="google Maps location"
						src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2248.8294084120583!2d11.431829216008727!3d53.999964779119176!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47ad5015e64e9e2d%3A0xb93c63244ce50d36!2sPromenade%201%2C%2018399%20Insel%20Poel!5e0!3m2!1sde!2sde!4v1713709438361!5m2!1sde!2sde"
						width="100%" height="220" style="border:0; border-radius: 0.5rem;" allowfullscreen loading="lazy">
					</iframe>
				</div>
				<a href="https://maps.google.com/?q=Promenade+1,+Insel+Poel" target="_blank" class="text-blue-600 underline">Karte in Google Maps öffnen</a>
			</div>
		</div>
	</main>
</div>

<style>
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeInUp {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
    .animate-fadeIn {
        animation: fadeIn 0.6s ease forwards;
    }
    .animate-fadeInUp {
        animation: fadeInUp 0.6s ease forwards;
    }
</style>