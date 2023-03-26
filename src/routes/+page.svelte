<script>
    import UserInput from "$lib/components/userInput.svelte";
    import TimelineSelector from "$lib/components/timelineSelector.svelte";
    import ShowLink from "$lib/components/showLink.svelte";
    // User input text
     /**
     * @type {string}
     */
    let userInput="";
    let user_entered_input=false;
    $: console.log("user input : ", userInput)
    $: {
        if(userInput != "") user_entered_input=true;
        else user_entered_input=false;
    }
    
    

    // active Timeline select
    /**
     * @type {{ link: string; }}
     */
    let data={link:""};

</script>
<div id="home">
    {#if user_entered_input && data.link==""}
    <TimelineSelector {userInput} bind:data={data}/>
    {:else if data.link!=""}
        <ShowLink {data}/>
    {:else}
        <UserInput bind:user_input={userInput}/>
    {/if}
</div>

<style>
    
    #home{
        position: relative;
        z-index: 1;
        align-items: center;
        justify-content: center;
        display: flex;
    }
</style>



