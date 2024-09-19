<script>
  const images = [
    {
      src: "https://images.pexels.com/photos/640781/pexels-photo-640781.jpeg?auto=compress&cs=tinysrgb&w=800",
      alt: "alt text",
    },
    {
      src: "https://images.pexels.com/photos/16025402/pexels-photo-16025402/free-photo-of-photo-of-fortaleza-canyon-in-brazil.jpeg?auto=compress&cs=tinysrgb&w=800",
      alt: "alt text",
    },
    {
      src: "https://images.pexels.com/photos/1743165/pexels-photo-1743165.jpeg?auto=compress&cs=tinysrgb&w=800",
      alt: "alt text",
    },
  ];
</script>

<!-- <img src={images[0].src} alt={images[0].alt} />
  <img src={images[1].src} alt={images[1].alt} />
  <img src={images[2].src} alt={images[2].alt} /> -->

<!-- en kortere måte å gjøre det samme på -->
<div class="gallery">
  {#each images as image}
    <img src={image.src} alt={image.alt} />
  {/each}
</div>

<style>
  .gallery {
    display: flex;
    flex-direction: column;
  }

  img {
    width: 50vw; /* 50% of the viewport width */
    max-width: 500px; /* Maximum width of 500px */
    height: auto;
    padding-top: 20px;
  }
</style>
