<script>
    /**
     * @type { {value:string, label:string} []}
     */
     export let options;
    /**
     * @type {string}
     */
     export let legend;
    export let userSelected = options[0].value;
    
</script>
<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Space+Mono&display=swap" rel="stylesheet">
</svelte:head>

<div id="tl-blc">
    <p id="tl-blc-title">{legend}</p>
    {#each options as option}
        <label class:tl-blc-radio={userSelected != option.value} class:tl-blc-radio-sel={userSelected == option.value}>
            <input type="radio" name="radio" bind:group={userSelected} value={option.value} />
            <span class="tl-blc-radio-cnt">{option.label}</span>
        </label>
    {/each}
</div>

<style>
    .tl-blc-radio-sel{
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 300;
        font-size: 10px;
        line-height: 100%;
        display: flex;
        align-items: center;
        letter-spacing: -0.02em;
        color: #FFFFFF;
        /* opacity: 0.5; */
        flex: none;
        order: 1;
        flex-grow: 0;
        margin:auto;
        accent-color: #AD52AA;
    }
    .tl-blc-radio{
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 300;
        font-size: 10px;
        line-height: 100%;
        display: flex;
        align-items: center;
        letter-spacing: -0.02em;
        color: #FFFFFF;
        opacity: 0.5;
        flex: none;
        order: 1;
        flex-grow: 0;
        margin:auto;
    }
    #tl-blc-title{
        font-family: 'Space Mono';
        font-style: normal;
        font-weight: 300;
        font-size: 10px;
        line-height: 100%;
        display: flex;
        align-items: center;
        letter-spacing: -0.02em;
        color: #D9D9D9;
        flex: none;
        order: 0;
        flex-grow: 0;
        margin: auto;
    }
    #tl-blc{
        display: flex;
        flex-flow: row wrap;
        /* flex-direction: row; */
        align-items: flex-start;
        padding: 10px;
        gap: 8px;
        width: 80%;
        /* height: 5vh; */
        background: rgba(255, 255, 255, 0.04);
        mix-blend-mode: normal;
        box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.33);
        backdrop-filter: blur(21.5px);
        border-radius: 58px;
        flex: none;
        order: 1;
        flex-grow: 0;
        /* flex-wrap: wrap; */
        animation-name: blc;
        animation-duration: 500ms;
    }

    /* @keyframes blc{
        0% {margin-top: 1000px;}
        25% {margin-top: 75px;}
        50% {margin-top: 50px;}
        75% {margin-top: 25px;}
        100% {margin-top: 10px;}
    } */
    @keyframes blc{
        0% {
            position: relative;
            top: 1000px;
        }
        10% {
            position: relative;
            top: 850px;
        }
        20% {
            position: relative;
            top: 600px;
        }
        30% {
            position: relative;
            top: 450px;
        }
        40% {
            position: relative;
            top: 300px;
        }
        50% {
            position: relative;
            top: 150px;
        }
        60% {
            position: relative;
            top: 100px;
        }
        70% {
            position: relative;
            top: 50px;
        }
        80% {
            position: relative;
            top: 25px;
        }
        90% {
            position: relative;
            top: 20px;
        }
        100% {margin-top: 10px;}
    }
    
    @media only screen and (min-width:321px) and (max-width: 768px) {
        #tl-blc-title{
            font-size: 15px;
            line-height: 100%;
        }
        .tl-blc-radio-sel{
            font-size: 15px;
            font-weight: 400;
        }
        .tl-blc-radio{
            font-size: 15px;
            font-weight: 400;
        }
    }

    @media only screen and (min-width:769px) and (max-width: 1200px) {
        #tl-blc-title{
            font-size: 20px;
            line-height: 100%;
        }
        .tl-blc-radio-sel{
            font-size: 20px;
            font-weight: 400;
        }
        .tl-blc-radio{
            font-size: 20px;
            font-weight: 400;
        }
    }

    @media only screen and (min-width:1201px) {
        #tl-blc-title{
            font-size: 24px;
            line-height: 100%;
        }
        .tl-blc-radio-sel{
            font-size: 24px;
            font-weight: 400;
        }
        .tl-blc-radio{
            font-size: 24px;
            font-weight: 400;
        }
    }

</style>