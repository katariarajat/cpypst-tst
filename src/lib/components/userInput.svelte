<script>
    export let user_input="";
</script>

<div id="userTextInputComponent">
    <input type="text" id="userTextInput" bind:value={user_input} placeholder="Paste / Write anything, Send anywhere....">
    <!-- <textarea id="userTextInput" cols="25" rows="2" bind:value={user_input} placeholder="Paste / Write anything, Send anywhere...."></textarea> -->
</div>

<style>
    #userTextInputComponent{

        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0px;
        background-color: transparent;
        background: transparent;
        /* gap: 73px; */
    }

    #userTextInput{
        width: 100%;
        text-size-adjust: auto;
        padding-top: 5%;
        background-color: transparent;
        border:none;
        /* background-color: #151517; */
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 200;
        font-size: 13px;
        line-height: 20px;
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

    @media only screen and (min-width:321px) and (max-width: 768px) {
        #userTextInput{
            font-size: 17px;
            line-height: 27px;
        }
    }

    @media only screen and (min-width:769px) and (max-width: 1200px) {
        #userTextInput{
            font-size: 22px;
            line-height: 47px;
        }
    }

    @media only screen and (min-width:1201px) {
        #userTextInput{
            font-size: 27px;
            line-height: 57px;
        }
    }
</style>