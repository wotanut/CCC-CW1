<script lang="ts">
    import { slide } from "svelte/transition";
    // import { Type } from "typescript";
    import Page from "./page.svelte";
	import Section from "./section.svelte";
	import Content from "./content.svelte";
	// import Page from "./page.svelte";

    export let currentTab = 0;
    export let printPage = 0;

    $: tab = currentTab

    // carousel then only needs a list of pages

    // take the list of pages as a prop
    export let pages :any[] = [];

    pages.forEach(page => {
        console.log(page)
        // console.log(page.componentData)
        console.log("------------------")
    });

    function updateTab(decrease=false) {
        if (decrease) {
            if (currentTab > 0) {
                currentTab--;
            }
        } else {
            if (currentTab < pages.length - 1) {
                currentTab++;
            }
        }
    }


</script>

<section class="carousel">

    {#each pages as page, index}
        {#if index === currentTab}

            <h1>Current Tab {index}</h1>

            <svelte:component this={page.component} {...page.componentData} />

            <!-- <svelte:component this={page.component} {...page.componentData} /> -->
            <!-- {console.log("Changing page" + page.component)} -->

            <!-- {#each pages as { component, componentData } (componentData.id)}
                <svelte:component this={component} {...componentData} />
            {/each} -->
            <!-- <Page {...page.componentData} /> -->

            <!-- <svelte:component this={page.component} {...page.props}></svelte:component> -->

            <!-- {#each page.componentData.sections as section} -->
                <!-- <p>Rendering section with ID {page.componentData.id}</p> -->
                <!-- <svelte:component this={section.component}/> -->
                <!-- <p>e</p> -->
            <!-- {/each} -->
            
            
        {/if}
    {/each}


    <section class="footer">
        <section class="dots">
            {#each pages as page, index}
    
                <button on:click={() => tab = index}>
    
                    <div class="dot {tab === index ? 'selected' : ''}"></div>
    
                </button>
                
            {/each}
        </section>

        <section class="controls">
            <button class="previous {tab == 0 ? 'disabled' : ''}" disabled={tab == 0} on:click={() => updateTab(true)}>Previous</button>
            <button class="next {tab == pages.length -1 ? 'disabled' : ''}" disabled={tab == pages.length -1} on:click={() => updateTab()}>Next</button>
        </section>

    </section>

</section>

<style>
    .controls {
        display: flex;
        justify-content: center;
    }

    .disabled {
        opacity: 0.5;
    }

    .disabled:hover {
        cursor: not-allowed;
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