<script>
    import Header from '../lib/components/header.svelte';
    import Footer from '../lib/components/footer.svelte';
    import Help from '$lib/components/help.svelte';
    

</script>

<div class="flex-box">
        <Header />
        <slot />
        <Footer />
        <Help />
</div>





<style>
    .flex-box{
        height: 95vh;
        display:flex;
        flex-direction: column;
        
    }
    /* .flex-box{
        display: flex;
        flex-direction: column;
        height: 95vh;
        width: 100%;
        justify-content: space-between;
        align-content: center;
    } */
    
    /* .footer{
        position: relative;
        bottom: 0;
    } */
    /* .main{
        position: relative;
        width: 100%;
        height: 40vh;
        background: #151517;
    } */
    
</style>