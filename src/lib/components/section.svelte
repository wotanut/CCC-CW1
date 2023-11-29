<script>
	import { slide } from "svelte/transition";

    /** 
     * @type {string}
    */ 
    export let title;
    export let backgroundColour = "var(--secondary)";
</script>

<section class="section" style="background-color: {backgroundColour};" transition:slide>

    <h1 class="title">{title}</h1>

    <!-- slot for section content -->
    <slot></slot>

</section>

<style>
    .section {
        /* background-color: color-mix(in srgb, steelblue 50%, #141e30 80%); */
        padding: 1rem;
        margin: 1rem;
        border-radius: 1rem;
        max-width: 25rem;
        /* box-shadow: darkblue 0 0 1rem; */
        box-shadow: var(--primary) 0 0 1rem;
        transition: all 0.5s ease-in-out;
        /* box-shadow: aqua 0 0 1rem; */
        
    }

    .section:hover {
        /* box-shadow: var(--secondary) 0 0 2rem; */
        scale: 1.01;
        transition: all 0.5s ease-in-out;
    }

    .title {
        text-align: center;
        font-size: large;
        text-decoration: underline;
    }
</style>