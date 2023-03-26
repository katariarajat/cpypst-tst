<script>
    import Header from '../lib/components/header.svelte';
    import Footer from '../lib/components/footer.svelte';
    import Help from '$lib/components/help.svelte';
    

</script>

<Header />
<Footer />
<slot />
<Help />



<style>
    
    /* .main{
        position: relative;
        width: 100%;
        height: 40vh;
        background: #151517;
    } */
    
</style>