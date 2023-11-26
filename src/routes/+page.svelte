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
</section>


<!-- choosing a pathfinding algorithm -->
<!-- NOTE: Instead of this possibly have web design process -->

<!-- The algorithm's process -->

<!-- testing the algorithm on towns -->

<style>
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
</style>