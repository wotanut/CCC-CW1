<script>
    import Carousel from "$lib/components/carousel.svelte";
    import Page from "$lib/components/page.svelte";
    import Image from "$lib/components/image.svelte";
    import Content from "$lib/components/content.svelte";

    import Pwegithed from "$lib/images/portsmouth/weighted.png";
    import Poverlay from "$lib/images/portsmouth/overlay.png";
    import Pdirectionalised from "$lib/images/portsmouth/directionalised.png";
    import Portsmouth from "$lib/images/portsmouth/portsmouth.png";
	import Section from "$lib/components/section.svelte";

    const section1 = [
        { component: Content, componentData: { content: `test` } }
    ]

    const page_1 = [
        { component: Image, componentData: { src: "https://picsum.photos/200", alt: "test" } },
        { component: Content, componentData: { content: `test` } }
    ]

    // const page1 = { component: Page, componentData: { id: 0, sections: [section1, image_1] } }
    const page2 = { component: Page, componentData: { id: 1, sections: [section1, section1] } }
    const page3 = { component: Page, componentData: { id: 1, sections: [section1, section1] } }

    const pages = [page_1, page2, page3]

</script>

<Section title="Preparing the graphs">
    <Carousel 
        {pages}
    />
</Section>