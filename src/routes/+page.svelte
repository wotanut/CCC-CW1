<script>
    import Carousel from "$lib/components/carousel.svelte";
    import Image from "$lib/components/image.svelte";
    import Section from "$lib/components/section.svelte";

    import portsmouthOverlay from "$lib/images/portsmouth/overlay.png";
</script>

<h1 class="title">
    Algorithm for Optimising Routes Based on Ethical Principles for Self-Driving Cars
</h1>

<section class="content">
    <!-- ethical framework-->
    
    <Section title="Ethical framework">
    
        <h3>
            Utilitarianism
        </h3>
    
        <p>
            For this model, I chose to use Utilitarianism. I primarily chose this framework due to it prioritising the greatest good
            for the greatest amount of people. This means that the model will heavily prioritise saftey of the people in the towns
            over the saftey of the driver. As a result of this, the model is more likely to chose a route that is longer but safer
            over a route that is shorter and more dangerous.
        </p>

        <p>

            Furthermore, as this framework is a form of consequentialism, it is the only model that is able to partially predict the
            outcome of a route. This is because the model is able to weight the outcome of a route based on the danger it will incur.
            When compared to the other proposed ethical frameworks, utilitarianism is the only framework that is able to be applied
            algorithmically, making it the only suibtable framework for this project.

        </p>

        <!-- notes: have ready the limitations of utilitarianism and rebuttals -->
    
    </Section>
    
    <!-- Preparing the graphs -->
    
    <Section title="Preparing the graphs" backgroundColour="red">
        <Image src="{portsmouthOverlay}" alt="An image of west Portsmouth with sevral major intersections marked as verticies and the roads as edges." />
    </Section>

    <!-- choosing a pathfinding algorithm -->
    <!-- Why this algorithm helps solve this problem -->
    <!-- NOTE: Instead of this possibly have web design process -->
    <Section title="Chosing a pathfinding algorithm">

    </Section>

    <!-- The algorithm's process -->
    <Section title="Algorithmic process">
        
    </Section>
    
    <!-- testing the algorithm on towns -->
    <Section title="Testing the algorithm">
        <!-- <Carousel>

        </Carousel> -->
    </Section>
</section>





<!-- only print -->

<section class="onlyPrint viewOnline">
   <p>View online <a href="blank">https://cw1.ccc.sambot.dev</a></p>
</section>

<style>

    .viewOnline {
        background-color: yellow;
        text-align: center;
        padding: 1rem;
    }

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
        /* flex-wrap: wrap;
        flex-basis: 25%; */
        max-height: 100vh;
    }

    @media screen
    {
        .onlyPrint {
            display: none;
        }
    }
</style>