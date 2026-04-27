<script>
    let now = $state(new Date());
    let separator = $state(':')
    let hourString = $derived(((now.getHours() % 12 || 12).toString().padStart(2, '0')))
    let minuteString = $derived(now.getMinutes().toString().padStart(2, '0'))
    let timeString = $derived(`${hourString}${separator}${minuteString} ${AMPM}`)
    let AMPM = $derived(now.getHours() < 12 ? 'AM' : 'PM')
    let celestialBody = $derived(6 <= now.getHours() && now.getHours() < 18 ? '☀︎' : '⏾')

    $effect(() => {
        const blink = setInterval(() => {
            now = new Date()
            separator = separator == ':' ? ' ' : ':'
        }, 1000)
        console.log(now)

        return () => clearInterval(blink)
    });
</script>

<style>
    .flip {
        transform: scale(-1, 1);
        display: inline-block;
    }
</style>

<!-- <div class="border-2 py-1 px-2 rounded-lg"> -->
    <span class="font-mono"><span class="flip mr-3">{celestialBody}</span>{timeString}</span>
<!-- </div> -->
