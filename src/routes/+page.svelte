<script lang="ts">
	import Cats from '$lib/components/Cats.svelte';
	import ComingSoon from '$lib/components/ComingSoon.svelte';
	import Highlight from '$lib/components/Highlight.svelte';
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import BlogPreview from '$lib/components/BlogPreview.svelte';

	import sleepingCat from '$lib/assets/sleeping_cat.png';
</script>

<style>
	.flip {
		transform: rotate(55deg) scale(-1, 1);
		display: inline-block;
	}
</style>

<div class="mx-auto grid w-full max-w-3xl grid-cols-1 gap-12 px-5 pb-16 font-carlito text-base leading-relaxed sm:px-8 sm:text-lg">
	<section class="space-y-6">
		<h1 class="font-radley text-5xl leading-tight text-foreground sm:text-6xl">
			<span class="italic">Hello</span>, I am
			<span class="underline decoration-accent decoration-2 underline-offset-4">Elijah</span>
		</h1>

		<p class="max-w-2xl">
			I'm a junior software engineer who recently graduated from the 
			<Highlight text="University of the Philippines" />. When I'm not writing code, I like to write 
			prose and poetry, play different instruments, and lift weights at the gym.
		</p>

		<p class="max-w-2xl">
			Welcome to my digital space; I hope to show you some parts and pieces of myself that
			I'm proud of. <span class="flip ml-1">𐔌˙.</span>
		</p>
	</section>

	<figure class="space-y-4">
		<div class="flex justify-center overflow-hidden rounded-lg border border-border bg-surface-strong px-3 py-5">
			<Cats />
		</div>
		<figcaption class="text-center text-sm text-muted sm:text-base">
			<span class="font-bold text-foreground">Figure 1.</span>
			"The best part about being alive is that sometimes there are cats."
		</figcaption>
	</figure>

	<div class="space-y-4">
		<SectionHeader id="blog" title="Blog" subtitle="prose, poetry, and all kinds of pondering" />
		
		<BlogPreview />
	</div>

	<div class="space-y-4">
		<SectionHeader
			id="projects"
			title="Projects"
			subtitle="some things i've made while tinkering with code"
		/>
		<ComingSoon />
	</div>

	<section id="resume" class="scroll-mt-28 space-y-4">
		<SectionHeader title="Resumé" subtitle="experience, education, and tools" />
		<ComingSoon label="Resume coming soon..." />
	</section>

	<!-- https://www.vhv.rs/dpng/d/480-4802563_cat-sleeping-clipart-black-and-white-svg-freeuse.png -->
	<!-- <div class="mx-auto mt-10">
		<img src={sleepingCat} alt="Sleeping cat illustration" class="h-28 opacity-90 sm:h-32" />
	</div> -->
</div>
