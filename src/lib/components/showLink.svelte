<script>
    /**
     * @type {any}
     */
     export let data;
     import CopyToClipboard from "../../static/symbols/copyToClipboard.svelte";
     import NewClip from "../../static/symbols/newClip.svelte";
     function clipBoard(){
        navigator.clipboard.writeText(data.link)
        .then(() => {
            alert("Link copied to clipboard");
            console.log("Text copied to clipboard");
        })
        .catch((err) => {
            alert("Failed to copy Link");
            console.error("Failed to copy text: ", err);
        });
     }
     function reload(){
        location.reload();
     }
</script>

<div id="shw-link-blc">
    <div id="disp-link">
        <p id="disp-link-url">{data.link}</p>
    </div>
    <div id="disp-time">
        <p id="time-val">Link will be destroyed once viewed</p>
    </div>
    <button id="clip-brd-btn" on:click={clipBoard}>
        <CopyToClipboard/>  
    </button>
    <button id="redirect" on:click={reload}>
        <NewClip/>
    </button>

    
</div>

<style>
    #redirect{
        box-sizing: border-box;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding: 8px 24px;
        gap: 8px;
        background: rgba(255, 255, 255, 0.06);
        border-radius: 54px;
    }
    #clip-brd-btn{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 16px 40px;
        gap: 12px;
        width: 30vw;
        height: 8vh;
        background: rgba(255, 255, 255, 0.06);
        box-shadow: 0px 6px 37px rgba(0, 0, 0, 0.38);
        border-radius: 40px;
        flex: none;
        order: 4;
        flex-grow: 0;
    }
    #time-val{
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 400;
        font-size: 24px;
        line-height: 100%;
        /* identical to box height, or 24px */

        display: flex;
        align-items: center;
        letter-spacing: -0.02em;

        color: #D9D9D9;

        opacity: 0.5;

        /* Inside auto layout */

        flex: none;
        order: 2;
        flex-grow: 0;
    }
    #disp-link-url{
        width: 10%;
        /* height: 32px; */
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 400;
        font-size: 20px;
        line-height: 100%;
        display: flex;
        align-items: center;
        text-align: center;
        justify-content: center;
        letter-spacing: -0.02em;
        color: #A5A5AD;
        flex: none;
        order: 0;
        flex-grow: 0
    }
    #disp-link{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        padding: 10px;
        gap: 8px;
        width: 40vw;
        height: 4vh;
        /* Secondary/80 */

        background: #2A2A2F;
        border-radius: 16px;

        /* Inside auto layout */

        flex: none;
        order: 0;
        flex-grow: 0;
    }
    #shw-link-blc{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0px;
        gap: 32px;

        width: 50vw;
    }
</style>