<script>
    import { slide } from "svelte/transition";

    // export let pages = [];

    let currentTab = 0;
</script>

<section class="carousel" in:slide>

    <slot></slot>



    <section class="footer">

        <!-- <section class="dots">
            {#each {length: pages} as _, page}
    
                <button on:click={() => currentTab = page}>{page}
    
                    {#if page === currentTab}
                        <span class="selected dot"></span>
                    {:else}
                        <span class="dot"></span>
                    {/if}
    
                </button>
                
            {/each}
        </section> -->


        <section class="controls">
            <button class="previous" on:click={() => currentTab--}>Previous</button>
            <button class="next" on:click={() => currentTab++}>Next</button>
        </section>

    </section>

</section>

<style>
    .controls {
        display: flex;
        justify-content: center;
    }

    .dots {
        display: flex;
        justify-content: center;
        padding: 3px;
    }

    .dot {
        height: 1px;
        width: 1px;
        border-radius: 2px;
        background-color: black;
    }

    .selected {
        background-color: aqua;
    }

    button {
        padding: 0.5rem;
        margin: 3px;
    }

    .previous {
        border-top-left-radius: 1rem;
        border-bottom-left-radius: 1rem;
        min-width: 5rem;
    }

    .next {
        min-width: 5rem;
        border-top-right-radius: 1rem;
        border-bottom-right-radius: 1rem;
    }

</style>