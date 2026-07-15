<script lang="ts">
	let { label = 'Under construction...' }: { label?: string } = $props();
</script>

<div class="rounded-lg border border-border bg-surface px-4 py-3 font-mono text-sm text-muted">
	{label}
</div>
