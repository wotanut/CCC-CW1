<script>
    import { slide } from "svelte/transition";

    /** 
     * @type {string}
    */ 
    export let title;
    export let id = 0;
</script>

<section class="section" transition:slide>

    <h1 class="title">{title}</h1>

    <!-- slot for section content -->
    <slot></slot>

</section>

<style>

</style>