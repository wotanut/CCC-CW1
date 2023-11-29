<script>
    import flowchart from "$lib/images/flowchart.png";

    import Image from "$lib/components/image.svelte";
    import Section from "$lib/components/section.svelte";
</script>

<Section title="Algorithmic process">
    <Image src={flowchart} alt="Flowchart of the algorithm" />

    <p>
        The algorithm is very simple. It takes a prepared graph and the start and end node. From the start node,
        it will traverse each edge and multiply the weight of that edge by the saftey of that weight. This is done
        to encourage the algorithm to take safer routes as opposed to shorter routes, because longer but safer routes
        are more likely to have a lower total score than shorter but more dangerous routes. The algoroithm will then
        add each of the total scores and the distance from the next edge to encourage the algorithm to only take routes
        that are relavant to it Finally the algorithm will check to see if the new node is the end node and repeat if not. 
        As a result, this algorithm is highly scalable and can be used on any size graph in a time efficient manner. 
    </p>

    <!-- why time over speed and why distance to edge is calculated at runtime rather than at build time-->

    <p>
        Importantly, distance is not a factor in this algorithm. This is because overall distance will become a constant
        rather than a variable as the distances will all be relative to each other. To counter this, the algorithm Instead
        takes the time it would take to travel an edge as a factor. This is because the time it takes to travel an edge
        will depend on the length, speed limit, traffic flow and traffic light timings. As a result, the algorithm requires
        less preperation and is more scalable.

        This algorithm heavily relies on the utilitarianism ethical framework, as explained to the left due to it's
        priorities, saftey over speed. This is because the algorithm will prioritise the saftey of the people in the
        towns over the drivers time.
    </p>

</Section>