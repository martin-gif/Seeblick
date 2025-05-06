<script>
	import {phone, email} from '$lib/data/contact.js';
</script>

<div class="flex min-h-screen  text-[#333] font-sans overflow-x-hidden">
	<!-- Content -->
	<main class="flex-1 mt-0  p-8">
		<!-- Hero -->
		<div class="bg-[#f6eee5] p-8 rounded-xl text-center mb-8">
			<h1 class="text-2xl font-bold text-[#a1886e]">Impressum</h1>
		</div>

		<!-- Impressum Info -->
		<div class="text-[#444] text-[1.1rem] space-y-8">
			<section>
				<h2 class="text-xl font-semibold text-[#a1886e] mb-4">Angaben gemäß § 5 TMG</h2>
				<p><strong>Firma:</strong> Traditionshaus Seeblick</p>
				<p><strong>Vertreten durch:</strong> Silke Menzel</p>
				<p><strong>Adresse:</strong> Promenande 1, 23999 Insel Poel</p>
				<p><strong>Kontakt:</strong></p>
				<p>Telefon: <a href="tel:{phone}">{phone}</a></p>
				<p>E-Mail: <a href="mailto:{email}">{email}</a></p>
			</section>

			<section>
				<h2 class="text-xl font-semibold text-[#a1886e] mb-4">Haftungsausschluss</h2>
				<p>
					Die Inhalte unserer Seiten wurden mit größter Sorgfalt erstellt. Für die Richtigkeit, Vollständigkeit und
					Aktualität der Inhalte können wir jedoch keine Gewähr übernehmen.
				</p>
			</section>

			<section>
				<h2 class="text-xl font-semibold text-[#a1886e] mb-4">Verantwortlich für den Inhalt nach § 55 Abs. 2 RStV</h2>
				<p>Silke Menzel (Adresse siehe oben)</p>
			</section>

			<section>
				<h2 class="text-xl font-semibold text-[#a1886e] mb-4">Haftung für Links</h2>
				<p>
					Unsere Webseite enthält Links zu externen Webseiten Dritter, auf deren Inhalte wir keinen Einfluss haben.
					Deshalb können wir für diese fremden Inhalte auch keine Gewähr übernehmen.
				</p>
			</section>

			<section>
				<h2 class="text-xl font-semibold text-[#a1886e] mb-4">Urheberrecht</h2>
				<p>
					Die durch die Seitenbetreiber erstellten Inhalte und Werke auf diesen Seiten unterliegen dem deutschen
					Urheberrecht.
				</p>
			</section>
		</div>
	</main>
</div>
