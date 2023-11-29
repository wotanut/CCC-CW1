<script>
    /** 
     * @type {string}
    */ 
    export let src;

    /**
     * @type {string}
    */ 
    export let alt;
</script>

<section class="image-section">
    <img class="image" {src} {alt}>
    <p class="description">{alt}</p>
</section>

<style>
    .description {
        /* text-align: center; centers the text */
        /* color: darkgray; */
        font-size: small; /* makes the text slightly smaller */
        /* max-width: 75%; makes the text flow onto the next line at 50% of the containers width */
    }

    .image-section {
        display: flex;
        flex-direction: column;
        align-items: center;
        /* gap:1rem */
    }

    .image {
        object-fit: contain;
        max-width: 100%;
    }
</style>