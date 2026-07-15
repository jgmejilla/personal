<script lang="ts">
	let { title, subtitle, id }: { title: string; subtitle: string; id?: string } = $props();
</script>

<section {id} class="scroll-mt-28">
	<h2 class="font-radley text-4xl sm:text-5xl">
		<span class="italic">
			{title}
		</span>
	</h2>
	<p class="font-carlito text-base text-muted italic sm:text-lg">{subtitle}</p>
</section>
