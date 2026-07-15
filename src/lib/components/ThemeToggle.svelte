<script lang="ts">
	import { browser } from '$app/environment';
	import { onMount } from 'svelte';

	type Theme = 'light' | 'dark';

	let theme = $state<Theme>('light');

	function applyTheme(nextTheme: Theme) {
		theme = nextTheme;
		document.documentElement.classList.toggle('dark', nextTheme === 'dark');
		document.documentElement.style.colorScheme = nextTheme;

		try {
			localStorage.setItem('theme', nextTheme);
		} catch {
			// The visual theme can still update when storage is unavailable.
		}
	}

	onMount(() => {
		theme = document.documentElement.classList.contains('dark') ? 'dark' : 'light';
	});
</script>

<button
	type="button"
	class="grid size-10 place-items-center rounded-full border border-border bg-surface/80 text-foreground shadow-sm transition hover:border-accent hover:text-accent focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-accent"
	aria-label={theme === 'dark' ? 'Switch to light mode' : 'Switch to dark mode'}
	aria-pressed={theme === 'dark'}
	onclick={() => browser && applyTheme(theme === 'dark' ? 'light' : 'dark')}
>
	<span class="text-lg leading-none" aria-hidden="true">{theme === 'dark' ? '☀︎' : '⏾'}</span>
</button>
