<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/Navbar.svelte';

	let { children } = $props();

</script>
<svelte:head>
	<title>elijah's corner</title>
	<link rel="icon" href={favicon}>
</svelte:head>


<Navbar />
<main class="min-h-screen bg-background pt-28 text-foreground transition-colors duration-200">
	{@render children()}
</main>
