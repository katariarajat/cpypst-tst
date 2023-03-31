<script>
    import { each } from "svelte/internal";
    import Radio from "./radio.svelte";
    import UserInput from "./userInput.svelte";
    
    const options = [{
		value: '00:00:00',
		label: 'When viewed',
	}, {
		value: '00:00:10',
		label: 'in 10 min',
	}, {
		value: '00:01:00',
		label: 'in 1 Hour',
	},{
		value: '07:00:00',
		label: 'in 1 week',
	},{
		value: '30:00:00',
		label: 'in 1 month',
	}
    ]
    /**
     * @type {string}
     */
     export let userInput;
    export let data;
    let radioValue="00:00:00";
    
    $: console.log(radioValue);
    // submit text 
    function onClick(){
        // send request
        let other = {
            userInput,
            radioValue
        }
        data = {
            link:"www.cpypst.com/YourLinkHere"
        }
    }
    
</script>
<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Space+Mono&display=swap" rel="stylesheet">
</svelte:head>

<div id="act-time-blc">
    <p id="act-time-blc-title">User  has  written  something</p> 
    <Radio {options} legend='Destroy it' bind:userSelected={radioValue}/>
    <button class="btn-submit" on:click={onClick}>
        <p id="btn-cnt">Get Link</p>
    </button>
    
</div>

<style>
    #act-time-blc-title{
        width: auto;
        height: auto;
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 150;
        font-size: 25px;
        line-height:17px;
        display: flex;
        align-items: center;
        text-align: center;
        letter-spacing: 0.01em;
        word-spacing: 0.3em;
        color: #FFFFFF;
        flex: none;
        order: 0;
        flex-grow: 0;
    }
    #btn-cnt{

        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 300;
        font-size: 10px;
        line-height: 47px;
        display: flex;
        align-items: center;
        letter-spacing: -0.04em;
        justify-content: center;
        color: #D9D9D9;
        backdrop-filter: blur(15.5px);
        flex: none;
        margin: 0;
        order: 0;
        flex-grow: 0;
    }
    .btn-submit{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        align-content: center;
        padding: 0.1% 1.5%;
        gap: 8px;
        width: auto;
        height: auto;
        background: rgba(255, 255, 255, 0.06);
        box-shadow: 0px 6px 37px rgba(0, 0, 0, 0.38);
        border-radius: 40px;

        /* Inside auto layout */

        flex: none;
        order: 3;
        flex-grow: 0;
    }
    #act-time-blc{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0px;
        gap: 33px;
        width: 100%;
    }
    
    @media only screen and (min-width:321px) and (max-width: 768px) {
        #act-time-blc-title{
            font-weight: 400;
            font-size: 15px;
            line-height:27px;
        }
        #btn-cnt{
            font-size: 15px;
        }
    }

    @media only screen and (min-width:769px) and (max-width: 1200px) {
        #act-time-blc-title{
            font-weight: 400;
            font-size: 20px;
            line-height:37px;
        }
        #btn-cnt{
            font-size: 20px;
        }
    }

    @media only screen and (min-width:1201px) {
        #act-time-blc-title{
            font-weight: 400;
            font-size: 25px;
            line-height:47px;
        }
        #btn-cnt{
            font-size: 25px;
        }
    }
    
    
</style>

