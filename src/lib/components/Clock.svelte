<script lang="ts">
	let now = $state(new Date());
	let separator = $state(':');
	let hourString = $derived((now.getHours() % 12 || 12).toString().padStart(2, '0'));
	let minuteString = $derived(now.getMinutes().toString().padStart(2, '0'));
	let amPm = $derived(now.getHours() < 12 ? 'AM' : 'PM');
	let timeString = $derived(`${hourString}${separator}${minuteString} ${amPm}`);
	let celestialBody = $derived(6 <= now.getHours() && now.getHours() < 18 ? '☀︎' : '⏾');

	$effect(() => {
		const blink = setInterval(() => {
			now = new Date();
			separator = separator === ':' ? ' ' : ':';
		}, 1000);

		return () => clearInterval(blink);
	});
</script>

<style>
	.flip {
		transform: scale(-1, 1);
		display: inline-block;
	}
</style>

<span class="font-mono text-sm text-muted">
	{timeString}
</span>
