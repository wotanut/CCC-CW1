<script>
    /**
     * importing the content components
    */
	import Ethics from "$lib/content/ethics.svelte";
	import Algorithm from "$lib/content/algorithm.svelte";
	import Preparing from "$lib/content/preparing.svelte";
	import Testing from "$lib/content/testing.svelte";
</script>

<h1 class="title">
    Algorithm for Optimising Routes Based on Ethical Principles for Self-Driving Cars
</h1>

<section class="content">
    <!-- ethical framework-->
    <Ethics />
    
    
    <!-- The algorithm's process -->
    <Algorithm />
    
    <!-- Preparing the graphs -->
    <Preparing />
    
    <!-- testing the algorithm-->
    <Testing />     

    <!-- Poster Design-->
    <!-- <WebDesign /> -->
</section>

<style>
    p {
        max-width: 50rem;
        margin-bottom: 30px;
    }

    @media (prefers-color-scheme: light) {
        :global(:root) {
            --text: #041a2a;
            --background: #d7ebf9;
            --primary: #bc5792;
            --secondary: #c4e5fd;
            --accent: #1a93ea;
        }
    }

    @media (prefers-color-scheme: dark) {
        :global(:root) {
            --text: #d5ebfb;
            --background: #061a28;
            --primary: #a8437e;
            --secondary: #02233b;
            --accent: #158ee5;
        }
    }

    .title {
        text-align: center;
        font-size: xx-large;
    }

    .content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
        overflow: auto;
        justify-content: center;
        max-height: 100vh;
    }

    @media screen
    {
        .onlyPrint {
            display: none;
        }
    }
</style>