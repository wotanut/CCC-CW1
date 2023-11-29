<script>
    import Section from "$lib/components/section.svelte";
    import Image from "$lib/components/image.svelte";

    import pweighted from "$lib/images/portsmouth/weighted.png";
</script>

<Section title="Preparing the Graph">
    <p>
        Because of the nature of the algorithm, it can only take in a graph that is both directionalised and weighted.
        As we've already established, each edge takes it's weight from the saftey of the road, rather than the length of it.
        This means the, although the graph is directionalised, it does not need to include the length of each edge in it's
        preperation as this can be calculated at runtime. Overall, this leads to less preperation of each graph leading to
        a more efficient process. Below is an example of what some graphs may look like after they have been prepared
    </p>

    <Image src={pweighted} alt="A weighted graph of Portsmouth" />

</Section>