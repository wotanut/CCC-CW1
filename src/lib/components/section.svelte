<script>
	import { slide } from "svelte/transition";


    /** 
     * @type {string}
    */ 
    export let title;
    export let backgroundColour = "red";
</script>

<section class="section" transition:slide>

    <h1 class="title">{title}</h1>

    <!-- slot for section content -->
    <slot></slot>


</section>

<style>
    .section {
        background-color: red;
        padding: 1rem;
        margin: 1rem;
        border-radius: 1rem;
        max-width: fit-content;
        /* box-shadow: aqua 0 0 1rem; */
        
    }

    .section:hover {
        box-shadow: aqua 0 0 2rem;
        transition: all 0.5s ease-in-out;
    }

    .title {
        text-align: center;
        font-weight: 300;
    }
</style>