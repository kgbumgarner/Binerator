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
*,
*::before,
*::after {
    box-sizing: border-box;
}

:root {
    --bs: 0.25em 0.25em 0.75em rgba(0, 0, 0, 0.25),
    0.125em 0.125em 0.25em rgba(0,0,0,.15);
}
    .image-container {
        max-height: 396px;
        max-width: 1400px;
        overflow: hidden;
        box-shadow: var(--bs);
        border: #E7E5E5 solid 4px;
    }

    main {
      display: flex; 
      flex-direction: column;
      margin: auto;
      align-items: center;
      margin: 40px; 
    }
</style>