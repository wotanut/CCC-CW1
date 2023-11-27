<script>
    import { slide } from "svelte/transition";

    /**
     * @type {[]}
     */
    export let pages = [];
    let currentTab = 0;
</script>

<section class="carousel" in:slide>



    <section class="footer">
        <section class="dots">
            {#each {length: pages} as _, page}
    
                <button on:click={() => currentTab = page}>{page}
    
                    {#if page === currentTab}
                        <span class="selected dot"></span>
                    {:else}
                        <span class="dot"></span>
                    {/if}
    
                </button>
                
            {/each}
        </section>

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
        gap: 5px;
        margin: 5px;
    }

    .dot {
        height: 10px;
        width: 10px;
        background-color: #bbb;
        border-radius: 50%;
        display: inline-block;
    }

    .selected {
        background-color: var(--primary);
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

    .footer {
        position: relative;
        bottom: 0%;
    }

    /* don't display the controls on print */
    @media print {
        .footer {
            display: none;
        }
    }
</style>