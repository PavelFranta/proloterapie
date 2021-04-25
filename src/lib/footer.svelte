<script>
import Email32 from "carbon-icons-svelte/lib/Email32";
import Phone32 from "carbon-icons-svelte/lib/Phone32";
</script>

<div class="w-full bg-gray-800">
<div class="md:h-56 max-w-7xl text-white p-6 md:p-12 flex flex-col md:flex-row items-stretch md:items-center md:justify-between m-auto">
  <div class="mb-5 md:mb-0">
    <h3>Dr. med. <strong>Jiří Půlpán</strong></h3>
    <span>Česká a německá atestace</span>
  </div>
  <div class="mb-5 md:mb-0">
    <h3 class="text-left"><strong>Kontakt</strong></h3>
    <a href="mailto:info@ortopedie-pulpan.com" class="flex underline mb-2">
      <Email32 class="hidden md:block mr-4" />info@ortopedie-pulpan.com
    </a>
    <a href="tel:608070706" class="flex underline">
      <Phone32 class="hidden md:block mr-4" />608 070 706
    </a>
  </div>
  <div>
    <h3 class="text-left"><strong>Ordinace</strong></h3>
    <p>Dykova 31</p>
    <p>Praha-Vinohrady</p>
    <p>10100</p>
  </div>
</div>
</div>