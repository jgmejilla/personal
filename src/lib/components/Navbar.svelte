<script lang="ts">
	import Clock from './Clock.svelte';
	import ThemeToggle from './ThemeToggle.svelte';

	const links = [
		{label: 'Home', href: '/'},
		{ label: 'Blog', href: '/blog' },
		{ label: 'Projects', href: '#projects' },
		{ label: 'Resumé', href: '#resume' }
	];
</script>

<header class="fixed inset-x-0 top-0 z-50 px-4 pt-3 font-carlito text-sm text-foreground sm:text-base">
	<nav
		class="mx-auto flex w-full max-w-3xl items-center justify-between gap-3 rounded-full border border-border bg-background/85 px-3 py-2 shadow-sm backdrop-blur-md sm:px-5"
		aria-label="Primary navigation"
	>
		<div class="flex min-w-0 items-center gap-1 sm:gap-3">
			{#each links as link}
				<a
					href={link.href}
					class="rounded-full px-3 py-2 transition hover:bg-surface hover:text-accent focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-accent"
				>
					{link.label}
				</a>
			{/each}
		</div>

		<div class="flex shrink-0 items-center gap-2">
			<div class="hidden sm:block">
				<Clock />
			</div>
			<ThemeToggle />
		</div>
	</nav>
</header>
