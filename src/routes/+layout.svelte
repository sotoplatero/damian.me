<script>
	import './layout.css';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" type="image/png" href="/favicon.ico" /></svelte:head>
{@render children()}
