<script>
    const frame0 = `                                  
        　　　　　／>　　 \フ   
        　　　　　| 　_　 _|            
        　 　　　／\` ミ＿xノ
        　　 　 /　　　 　 |      
        　　　 /　 ヽ　　 ﾉ                
        　 　 │　　|　|　|
        　／￣|　　 |　|　|
        　| (￣ヽ＿ヽ)__) __)
        　＼二つ
     the best part about life is that    
         sometimes there are cats
`
    const frame1 = `                                  
        　　　　　／>　　 \フ   
        　　　　　| 　_　 _| z           
        　 　　　／\` ミ＿xノ
        　　 　 /　　　 　 |      
        　　　 /　 ヽ　　 ﾉ                
        　 　 │　　|　|　|
        　／￣|　　 |　|　|
        　| (￣ヽ＿ヽ)__) __)
        　＼二つ
     the best part about life is that    
         sometimes there are cats
`
    const frame2 = `                                  
        　　　　　／>　　 \フ   z
        　　　　　| 　_　 _| z           
        　 　　　／\` ミ＿xノ
        　　 　 /　　　 　 |      
        　　　 /　 ヽ　　 ﾉ                
        　 　 │　　|　|　|
        　／￣|　　 |　|　|
        　| (￣ヽ＿ヽ)__) __)
        　＼二つ
     the best part about life is that    
         sometimes there are cats
`

const frame3 = `                           z       
        　　　　　／>　　 \フ   z
        　　　　　| 　_　 _| z           
        　 　　　／\` ミ＿xノ
        　　 　 /　　　 　 |      
        　　　 /　 ヽ　　 ﾉ                
        　 　 │　　|　|　|
        　／￣|　　 |　|　|
        　| (￣ヽ＿ヽ)__) __)
        　＼二つ
     the best part about life is that    
         sometimes there are cats
`

const frames = [frame0, frame1, frame2, frame3]
let selectedFrameIndex = $state(0)
let selectedFrame = $derived(frames[selectedFrameIndex])


setInterval(() => {
    selectedFrameIndex = (selectedFrameIndex + 1) % frames.length;
}, 2000)



let now = $state(new Date())
let hours = $derived(now.getHours())
let minutes = $derived(now.getMinutes())
let colon = $state(true)
let time = $derived(`${hours}${colon ? ':' : ' '}0${minutes}`)

setInterval(() => {
    now = new Date()
    colon = !colon
}, 500)



</script>

<pre>
    {@html time}
</pre>

<pre>
    {@html selectedFrame}
</pre>




