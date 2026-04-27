<script>
    const frames = [
`        ／>　　 \フ   
　　 　 | 　_　 _|     
 　　　／\` ミ＿xノ
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`,

`        ／>　　 \フ   
　　 　 | 　_　 _|     
 　　　／\` ミ＿xノ z
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`,

`        ／>　　 \フ   
　　 　 | 　_　 _|   z   
 　　　／\` ミ＿xノ z
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`,

`        ／>　　 \フ    z  
　　 　 | 　_　 _|   z   
 　　　／\` ミ＿xノ z
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`,

`        ／>　　 \フ   
　　 　 | 　_　 _|   z   
 　　　／\` ミ＿xノ z
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`,

`        ／>　　 \フ   
　　 　 | 　_　 _|     
 　　　／\` ミ＿xノ z
　 　 /　　　 　 |             
　　 /　 ヽ　　 ﾉ        ／7、
 　 │　　|　|　|       （ﾟ､ ｡ ７
／￣|　　 |　|　|        |、ﾞ ~ヽ
| (￣ヽ＿ヽ)__) __)      じし__, )ノ
　＼二つ`,
];

let frameNo = $state(0); 
let frame = $derived(frames[frameNo])

$effect(() => {
    const switchFrame = setInterval(() => {
        frameNo = (frameNo + 1) % frames.length
    }, 1500)
    console.log(frame)
    
    return () => clearInterval(switchFrame)
});

</script>

<pre class="w-auto text-md md:text-xl text-darkgray">{frame}</pre> 