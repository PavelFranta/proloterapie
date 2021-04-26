<script>
  let y;
</script>

<svelte:window bind:scrollY={y}/>
<nav class="fixed w-full z-10 flex items-center bg-white text-black md:text-white" class:scrollYBiggerThanZero="{y}" class:scrollZero="{y === 0}">
	<a href="/" class="text-2xl pl-4">PROLOTERAPIE</a>
</nav>
<style>
	nav {
		background-color: transparent;
		font-family: 'Helvetica Neue', 'Helvetica', 'Arial', sans-serif;
		height: 80px;
	}

  .scrollYBiggerThanZero {
    transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 500ms;

    @apply bg-white;
    @apply text-black
  }

  .scrollZero {
    transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 500ms;

    @apply bg-transparent;
    @apply text-white
  }

</style>
