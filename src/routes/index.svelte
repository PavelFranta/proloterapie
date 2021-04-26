<script>
	let pragueSrc = './praha.jpg';
	import Network_432 from 'carbon-icons-svelte/lib/Network_432';
	import Sunny32 from 'carbon-icons-svelte/lib/Sunny32';
	import ReminderMedical32 from 'carbon-icons-svelte/lib/ReminderMedical32';
	import Contact from '$lib/contact.svelte';
</script>

<div class="prague">
	<img src={pragueSrc} alt="skull" class="w-full xl:big-resolution" />
</div>
<h2 class="px-6 py-4 leading-10 text-2xl text-center bg-white">
	Proloterapie je léčebná metoda založená na stimulaci přirozeného procesu hojení těla.
</h2>
<div class="triangle-down" />
<div class="max-w-screen-lg m-auto">
	<div
		class="bg-black flex flex-col md:flex-row justify-between py-8 text-center text-white"
	>
		<div class="flex-1 p-6">
			<ReminderMedical32 class="text-green-900 m-auto mb-6 h-16 w-16" />
			<h4 class="mb-4 font-bold text-3xl">S čím mi pomůže?</h4>
			<p class="flex-1">
				Proloterapie se ve Spojených státech a v západní Evropě již více než 50 let úspěšně používá
				při léčbě poškozených vazů, šlach, kloubů a meziobratlových plotének.
			</p>
		</div>
		<div class="flex-1 p-6">
			<Sunny32 class="text-green-900 m-auto mb-6 h-16 w-16" />
			<h4 class="mb-4 font-bold text-3xl">Výhody této metody</h4>
			<p class="flex-1">
				Hlavní výhodou proloterapie je její vysoká úspěšnost (80%), minimální vedlejší účinky a
				ambulantní styl léčby. Většinou není nutná ani pracovní neschopnost.
			</p>
		</div>
		<div class="flex-1 p-6">
			<Network_432 class="text-green-900 m-auto mb-6 h-16 w-16" />
			<h4 class="mb-4 font-bold text-3xl">Jak se to provádí?</h4>
			<p class="flex-1">
				Proloterapeutická stimulace se provádí sérií injekcí, jejichž hlavní složkou je cukerný
				roztok z dextrózy.
			</p>
		</div>
	</div>
</div>
<h2 class="px-6 py-4 leading-10 text-2xl text-center bg-white">Detailní popis léčby</h2>
<div class="triangle-down" />
<div class="bg-green-900">
	<div class="max-w-screen-lg m-auto lg:flex md:items-center text-white treatment-detail py-10 md:py-20 bg-green-900">
		<div>
		<p>
			Pacientovi je na léčené místo injekčně vpraven roztok dextrózy, který vytvoří lokální zánět.
		</p>
		<p>
			Tím dojde k mobilizací imunitního systému, který zasáhne a začne toto místo intenzivně
			regenerovat.
		</p>
	</div>
		<p>Injekční aplikace trvá několik málo vteřin a je velmi dobře snášena i méně statečnými.</p>
		<p>
			Pro hluboké proléčení je třeba aplikaci v týdenních intervalech několikrát opakovat. Maximálně
			však 10 týdnů.
		</p>
		<p>Účinek léčby proloterapií je trvalý a není třeba jej obnovovat.</p>
	</div>
</div>
<h2 class="px-6 py-4 leading-10 text-2xl text-center bg-white">
	Domluvte si termín své konzultace
</h2>
<div class="triangle-down" />
<!-- <Contact /> -->
<style>
	.prague {
		max-height: 500px;
		overflow: hidden;
	}

	@media only screen and (min-width: 1800px) {
		.prague img {
			position: relative;
			top: -250px;
		}
	}

	@media only screen and (min-width: 2730px) {
		.prague img {
			position: relative;
			top: -400px;
		}
	}

	.prague img {
		max-height: 100%;
		max-width: 100%;
	}

	.triangle-down {
		position: absolute;
		left: 30px;
		width: 0;
		height: 0;
		border-left: 30px solid transparent;
		border-right: 30px solid transparent;
		border-top: 30px solid white;
	}

	.treatment-detail p {
		@apply px-6;
		@apply py-2;
	}
</style>
