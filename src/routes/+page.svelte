<script>
    import Carousel from "$lib/components/carousel.svelte";
    import Image from "$lib/components/image.svelte";
    import Section from "$lib/components/section.svelte";

    import portsmouthOverlay from "$lib/images/portsmouth/overlay.png";
</script>

<h1 class="title">
    Demo
</h1>

<section class="content">
    <!-- ethical framework-->
    
    <Section title="Ethical framework">
    
        <h3>
            Utilitarianism
        </h3>
    
        <p>
            For this model, I chose to use Utilitarianism. I primarily chose this model due to it prioritising the greatest good for the greatest amount of people. 
        </p>
    
        <!-- <Carousel /> -->
    </Section>
    
    <!-- Preparing the graphs -->
    
    <Section title="Preparing the graphs" backgroundColour="red">
        <Image src="{portsmouthOverlay}" alt="An image of west Portsmouth with sevral major intersections marked as verticies and the roads as edges." />
    </Section>

    <!-- choosing a pathfinding algorithm -->
    <!-- NOTE: Instead of this possibly have web design process -->
    <Section title="Chosing a pathfinding algorithm">

    </Section>

    <!-- The algorithm's process -->
    <Section title="Algorithmic process">

    </Section>
    
    <!-- testing the algorithm on towns -->
    <Section title="Testing the algorithm">
        <Carousel>
            
        </Carousel>
    </Section>
</section>





<!-- only print -->

<section class="onlyPrint">
    <h1>
        This site looks better online
    </h1>
    <a href="blank">
        https://cw1.ccc.sambot.dev
    </a>
</section>

<style>

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

    :global(:root) {
        --warning: rgba(255, 255, 0, 0.825), 255, 0;
    }

    .title {
        text-align: center;
        font-size: xx-large;
    }

    .content {
        display: flex;
        overflow: auto;
        justify-content: center;
        flex-wrap: wrap;
    }

    @media screen
    {
        .onlyPrint {
            display: none;
            background-color: var(--warning);
        }
    }
</style>