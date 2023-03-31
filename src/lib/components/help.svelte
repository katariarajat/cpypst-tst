<script>
    import HelpBox from "./helpBox.svelte";
    let showBox = false;
    function showHelpBox(){
        showBox = true;
        console.log("showHelpBox");
    }
    function hideHelpBox(){
        showBox = false;
        console.log("hideHelpBox");
    }
</script>

{#if showBox}
<div id="hlp-blc">
    <HelpBox />
</div>
{/if}
    
<!-- <HelpBox /> -->
<div id="hlp-btn" on:mouseenter={showHelpBox} on:mouseleave={hideHelpBox}>
    <span id="hlp-btn-txt">?</span>
</div>
    


<style>
    #hlp-blc{
        position: absolute;
        bottom: 14vh;
        right: 8vh;
        /* Note: backdrop-filter has minimal browser support */
        z-index: 0;
    }
    #hlp-btn{
        border-radius: 100%;
        position: absolute;
        width: 3.5%;
        height: 4%;
        bottom: 10vh;
        right: 10vh;
        background: rgba(255, 255, 255, 0.06);
        box-shadow: 0px 6px 37px rgba(0, 0, 0, 0.38);
        z-index: 5;
        align-items: center;
        justify-content: center;
    }
    
    
    #hlp-btn-txt{
        border-radius: 100%;
        font-family: 'Source Code Pro';
        font-style: normal;
        font-weight: 600;
        font-size: 22px;
        line-height: 40px;
        display: flex;
        align-items: center;
        justify-content: center;
        letter-spacing: -0.04em;

        /* Main/White */

        color: #FFFFFF;

        backdrop-filter: blur(15.5px);
        /* Note: backdrop-filter has minimal browser support */
    }
</style>