<script>
	import Image from "$lib/components/image.svelte";
    import Section from "$lib/components/section.svelte";

    import routeAcrossTownA from "$lib/images/routes/route_across_town_a.png";

</script>

<Section title="Testing the algorithm">
    
    <Image src={routeAcrossTownA} alt="A route across town A. The route follows the red line.
    This is the most optimal route across this town according to the algorithm. This is due to the 
    multiplication of the saftey weighting. The hot pink line gives a weighting of (8 * 2) + (7*2) = 30 (assuming
    each road takes 2 minutes), wheras the red line gives a total of (7 * 2) + (4 * 2) = 22 .The green line gives
    (22 * 2) + (4 * 2) = 52 as it is the most dangerous route. The red line is therefore the most optimal
    as it keeps the most people safe whilst keeping the driver happy.
    " />

</Section>