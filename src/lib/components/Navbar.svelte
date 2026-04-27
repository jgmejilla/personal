<script>
    import Clock from "./Clock.svelte";
</script>

<div class="text-darkgray font-carlito text-xl fixed top-0 w-full flex justify-center items-center ">
    <div class="px-10 py-3 flex w-1/2 justify-between items-center bg-cream/10 backdrop-blur-sm rounded-b-2xl">
        <div class="gap-10 flex justify-center items-center ">
            <h3>Blog</h3>
            <h3>Projects</h3>
            <h3>Resume</h3>
        </div>
        <div>
            <Clock />
        </div>
    </div>
</div> 