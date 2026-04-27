<script>
    import Highlight from "$lib/components/Highlight.svelte";
    import SectionHeader from "$lib/components/SectionHeader.svelte";
    import Cats from "$lib/components/Cats.svelte";
</script>

<style>
    .flip {
        transform: rotate(55deg) scale(-1, 1);
        display: inline-block;
    }
</style>

<div class="text-lg font-carlito md:px-10 md:w-1/2 w-3/4 gap-10 mx-auto 
grid grid-cols-1">
    <div class="space-y-6 leading-relaxed ">
        <h1 class="text-5xl font-radley">
            <span class="italic">
                Hello
            </span>, 
            I am 
            <span class="underline decoration-lightbrown">
                Elijah
            </span>
            
        </h1>
        <p class="mt-10">
            I'm an undergraduate computer science student studying at the
            <Highlight text="University of the Philippines" />. 
            I Iike 
            <Highlight text="cats" /> (see below), 
            <Highlight text="playing instruments" />, and 
            <Highlight text="moving" /> metal circles at the gym.
                
            Welcome to my digital space; I hope to show you a few parts 
            and pieces of myself. <span class="ml-[3px] flip">𐔌˙.</span>
        </p>
    </div>
    <div>
    <div class="mt-2 mb-5 flex justify-center ">
        <Cats />    
    </div>
    <p class="mt-1 md:mb-10 italic text-center text-sm md:text-lg text-lightgray">The best part about life is that sometimes there are cats.</p>
    </div>
    <SectionHeader title="Blog" subtitle="prose, poetry, and all kinds of words"/>
    <pre class="text-lightgray">Under construction...</pre>
    
    <SectionHeader title="Projects" subtitle="some neat things i've scrapped together"/>
    <pre class="text-lightgray">Under construction...</pre>

    
    
</div>

    
<!-- insert ascii art here -->

