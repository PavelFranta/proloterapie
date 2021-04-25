<script>
	 import Menu32 from "carbon-icons-svelte/lib/Menu32";

	// Show mobile icon and display menu
	let showMobileMenu = false;
  let y;

	const navItemsRight = [
    { label: 'PROLOTERAPIE', href: '/' },
		{ label: 'kontakt', href: '/contact' }
	];

	// Mobile menu click event handler
	const handleMobileIconClick = () => (showMobileMenu = !showMobileMenu);

	const handleClick = () => {
    if (window.innerWidth < 480) {
      showMobileMenu = false;
    }
  }
</script>

<svelte:window bind:scrollY={y}/>
<nav class="fixed w-full z-10 bg-white text-black md:text-white" class:scrollYBiggerThanZero="{y}" class:scrollZero="{y === 0}">
	<div class="inner font-mono w-full">
    <div class="w-full flex justify-between">
      <a href="/" class="prolo-hidden text-2xl">PROLOTERAPIE</a>
      <div class="prolo-hidden">
        <Menu32 on:click={handleMobileIconClick} class="h-16 w-16 -mt-3"/>
      </div>
    </div>
		<div class="w-full">
			<ul class={`flex justify-between navbar-list${showMobileMenu ? ' mobile' : ''}`}>
				{#each navItemsRight as item}
					<li>
						<a on:click={handleClick} href={item.href} class={showMobileMenu ? "text-white" : ""}>{item.label}</a>
					</li>
				{/each}
			</ul>
		</div>
	</div>
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

  .scrollBiggerThenZeroHamburgerMenu {
    background-color: black;
  }

  .scrollZero {
    transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 500ms;

    @apply bg-transparent;
    @apply text-white
  }

	.inner {
		display: block;
		padding: 20px;
		box-sizing: border-box;
		height: 5rem;
	}

	.navbar-list {
		display: none;
		margin: 0;
		padding: 0 40px;
	}

	.navbar-list.mobile {
    padding-top: 1rem;
		background-color:black;
		position: fixed;
		display: block;
		height: 100%;
    width: 100%;
		bottom: 0;
		left: 0;
	}

	.navbar-list li {
		list-style-type: none;
		position: relative;
	}

	.navbar-list li:before {
		content: '';
		position: absolute;
		bottom: 0;
		left: 0;
		height: 1px;
		background-color: black;
	}

	.navbar-list a {
		text-decoration: none;
		display: flex;
		height: 45px;
		align-items: center;
		padding: 0 10px;
		font-size: 24px;
	}

	@media only screen and (min-width: 480px) {
		.navbar-list {
			display: flex;
			padding: 0;
		}

		.navbar-list a {
			display: inline-flex;
		}

    .prolo-hidden {
      display: none;
    }
  }
</style>
