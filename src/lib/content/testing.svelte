<script>
	import Image from "$lib/components/image.svelte";
    import Section from "$lib/components/section.svelte";

    // example routes
    import routeAcrossTownA from "$lib/images/routes/route_across_town_a.png";
    import routeAcrossTownB from "$lib/images/routes/route_across_town_b.png";

</script>

<Section title="Testing the algorithm">

    <Image src={routeAcrossTownA} alt="A route across town A. The route follows the red line.
    This is the most optimal route across this town according to the algorithm. This is due to the 
    multiplication of the saftey weighting. The hot pink line gives a weighting of (8 * 2) + (7*2) = 30 (assuming
    each road takes 2 minutes), wheras the red line gives a total of (7 * 2) + (4 * 2) = 22 .The green line gives
    (22 * 2) + (4 * 2) = 52 as it is the most dangerous route. The red line is therefore the most optimal
    as it keeps the most people safe whilst keeping the driver happy.
    " />

    <Image src={routeAcrossTownB} alt="A route across town B. This time, the hot pink line represents the most optimal route.
    Assuming a weighting of 2 minutes per road, the red line has a weighting of (8 * 2) + (5 * 2) = 26 and the green line
    has a weighting of (1*2) + (2*2) + (20*2) + (5*2) = 60, wheras the hot pink line has a weighting of (5*2) + (2*2) + (2*6) = 24.
    "/>

</Section>