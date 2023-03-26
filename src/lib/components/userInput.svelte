<script>
    export let user_input="";
</script>

<div id="userTextInputComponent">
    <textarea id="userTextInput" cols="50" rows="2" bind:value={user_input} placeholder="Paste / Write anything, Send anywhere...."></textarea>
</div>

<style>
    #userTextInputComponent{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0px;
        /* gap: 73px; */
    }

    #userTextInput{
        text-size-adjust: auto;
        padding-top: 10vh;
        border-color: transparent;
        outline: none;   
        background-color: #151517;
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 200;
        font-size: 30px;
        line-height: 27px;
        display: flex;
        align-items: center;
        text-align: center;
        resize: none;
        outline: none;
        border: none;
        /* Main/White */
        opacity: 0.6;
        color: #FFFFFF;


        /* Inside auto layout */

        flex: none;
        order: 0;
        flex-grow: 0;
    }
</style>