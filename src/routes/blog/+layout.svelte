<script>
    let { children } = $props();
</script>

<div class="mx-auto grid w-full max-w-3xl grid-cols-1 gap-12 pb-16 font-carlito text-base leading-relaxed sm:px-8 sm:text-lg">
    {@render children()}
</div>