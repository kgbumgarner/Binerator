<!-- Size of images should be 1584x396-->

<script>
    /* Variables */
    let images = [
        { src:'/Images/blurredCity.jpeg', alt:"Blurred City" },
        { src:'/Images/bubbles.jpeg', alt:"Bubbles" },
        { src:'/Images/cityLookUp.jpeg', alt:"City Bottom View" },
        { src:'/Images/linesColors.png', alt:"Colored Lines" },
        { src:'/Images/oceanSunset.jpeg', alt:"Ocean Sunset" },
        { src:'/Images/snow.jpeg', alt:"Snow" },
    ];
    let image = images[0];
    
    /* Get random image after clicking generate button */
    function generateRandomImage() {
        let size = images.length;
        let index = Math.floor((Math.random() * size));
        console.log(index);
        image = images[index];
    }
</script>

<main>
    <div class='image-container'>
        <img src={image.src} alt={image.alt}/>
    </div>

    <button on:click={generateRandomImage}>Generate</button>
</main>

<style>
    .image-container {
        max-height: 396px;
        overflow: hidden;
    }
</style>