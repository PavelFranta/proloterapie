<script>
	let pragueSrc = './praha.jpg';
	import Network_432 from 'carbon-icons-svelte/lib/Network_432';
	import Sunny32 from 'carbon-icons-svelte/lib/Sunny32';
	import ReminderMedical32 from 'carbon-icons-svelte/lib/ReminderMedical32';
</script>

<div class="prague">
	<img src={pragueSrc} alt="skull" class="w-full xl:big-resolution"/>
</div>
<h2 class="px-6 py-4 leading-10 text-2xl text-center bg-white">
	Proloterapie je léčebná metoda založená na stimulaci přirozeného procesu hojení těla.
</h2>
<div class="triangle-down" />
<div class="max-w-screen-lg m-auto">
		<div class="bg-black md:h-96 flex flex-col md:flex-row justify-between py-8 text-center text-white">
			<div class="flex-1 p-6">
				<ReminderMedical32 class="text-green-900 m-auto mb-6 h-16 w-16" />
				<h4 class="mb-4 font-bold text-3xl">Jak se to provádí</h4>
				<p class="flex-1">
					Tato stimulace se provádí sérií injekcí, jejíž hlavní složkou je roztok dextrózy, cukru.
				</p>
			</div>
			<div class="flex-1 p-6">
				<Sunny32 class="text-green-900 m-auto mb-6 h-16 w-16" />
				<h4 class="mb-4 font-bold text-3xl">Výsledky a pohodlí</h4>
				<p class="flex-1">
					Hlavní výhodou této metody je vysoká úspěšnost( 80%), minimální vedlejší účinky a
					ambulantní styl léčby, většinou není nutná ani pracovní neschopnost.
				</p>
			</div>
			<div class="flex-1 p-6">
				<Network_432 class="text-green-900 m-auto mb-6 h-16 w-16" />
				<h4 class="mb-4 font-bold text-3xl">Historie</h4>
				<p class="flex-1">
					Proloterapie se úspěšně používá již více než 50 let u léčby poškozených vazů, šlach,
					kloubů a meziobratlových plotének hlavně ve Spojených státech a západní Evropě.
				</p>
			</div>
		</div>
	</div>
<h2 class="px-6 py-4 leading-10 text-2xl text-center bg-white">Detailní popis léčby</h2>
<div class="triangle-down" />
<div class="bg-green-900">
	<div class="max-w-screen-lg m-auto text-white treatment-detail py-10 md:py-20 bg-green-900">
		<p>
			Pacientovi je na léčené místo injekčně vpraven roztok dextrózy, který vytvoří lokální zánět,
			čímž mobilizuje síly imunitního systému aby zasáhl a začal toto místo hromadně regenerovat
		</p>
		<p>Injekční aplikace trvá několik málo vteřin a je velmi dobře snášena i méně statečnými :)</p>
		<p>
			Pro hluboké proléčení je třeba aplikaci několikrát opakovat v týdenních intervalech (maximálně
			však 10 týdnů)
		</p>
		<p>Účinek léčby proloterapií je následně trvalý a není třeba jej obnovovat.</p>
	</div>
</div>
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
