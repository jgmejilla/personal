<script>
    import Highlight from "$lib/components/Highlight.svelte";
    import SectionHeader from "$lib/components/SectionHeader.svelte";
    import Cats from "$lib/components/Cats.svelte";

    const cats = `        ／>　　 \フ   
　　 　 | 　_　 _|     
 　　　／\` ミ＿xノ
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`;
</script>

<div class="text-lg font-carlito py-20 md:px-10 md:w-1/2 w-3/4 gap-5 mx-auto 
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
        <p>
            I'm an undergraduate computer science student studying at the
            <Highlight text="University of the Philippines" />. 
            I Iike 
            <Highlight text="cats" /> (see below), 
            <Highlight text="playing instruments" />, and 
            <Highlight text="moving" /> metal circles at the gym.

            Welcome to my digital space; I hope to show you a few parts 
            and pieces of myself <span class="ml-1">𐔌˙.</span>
        </p>
    </div>
    <div>
    <div class="flex justify-center">
        <Cats />    
    </div>
    <p class="mt-1 italic text-center text-sm md:text-lg text-lightgray">The best part about life is that sometimes there are cats.</p>
    </div>
    <SectionHeader title="Blog" subtitle="prose, poetry, and all kinds of words"/>
    <SectionHeader title="Projects" subtitle="some neat things i've scrapped together"/>
</div>