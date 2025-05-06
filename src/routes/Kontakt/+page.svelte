<script>
	import {phone, email} from '$lib/data/contact.js';
</script>

<div class="flex flex-col   text-[#333] font-sans">
		<main class="flex-1 mt-0  p-8 animate-fadeIn">
		<div class="bg-[#f6eee5] rounded-lg p-8 text-center mb-8 animate-fadeIn">
			<h1 class="text-2xl font-semibold text-[#a1886e] mb-2">Traditionshaus Seeblick</h1>
			<p class="text-lg text-[#666]">So erreichen Sie uns.</p>
		</div>

		<div class="bg-[#fdf5ec] rounded-lg shadow-md p-8 mb-8 animate-fadeIn">
			<p class="mb-4"><strong>🏡 Adresse:</strong><br />
				Traditionshaus Seeblick<br />
				Promenande 1<br />
				23999 Insel Poel (OT Schwarzer Busch)
			</p>
			<p class="mb-4"><strong>📞 Telefon:</strong><br /><a href="tel:{phone}">{phone}</a></p>
			<p class="mb-4"><strong>📧 E-Mail:</strong><br /><a href="mailto:{email}">{email}</a></p>
			<p><strong>🕒 Öffnungszeiten:</strong><br />
				Täglich 11:00 – 20:00 Uhr<br />
				Mittwochs Ruhetag
			</p>
		</div>

		<div class="rounded-lg shadow-lg overflow-hidden animate-fadeIn">
			<iframe
				src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2248.8294084120583!2d11.431829216008727!3d53.999964779119176!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47ad5015e64e9e2d%3A0xb93c63244ce50d36!2sPromenade%201%2C%2018399%20Insel%20Poel!5e0!3m2!1sde!2sde!4v1713709438361!5m2!1sde!2sde"
				class="w-full h-[400px]"
				allowfullscreen=""
				loading="lazy"
				referrerpolicy="no-referrer-when-downgrade"
			></iframe>
		</div>
	</main>
</div>

<!-- Optional: Toggle button (can be placed elsewhere if needed) -->
<!--
<button class="fixed top-4 left-4 z-20 bg-[#f3e9dd] p-2 rounded shadow-md md:hidden" on:click={toggleSidebar}>
	☰
</button>
-->

<style>
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }
    .animate-fadeIn {
        animation: fadeIn 0.6s ease-out;
    }
</style>
