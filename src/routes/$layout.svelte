<script>
	import '../app.postcss';
	import Footer from '$lib/footer.svelte';
	import Nav from '../lib/nav.svelte';
</script>

<Nav />
	<slot />
<Footer />
