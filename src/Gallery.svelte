<script>
  const images = [
    {
      src: "https://storage.googleapis.com/pod_public/1300/194530.jpg",
      alt: "alt text",
    },
    {
      src: "https://storage.googleapis.com/pod_public/1300/203048.jpg",
      alt: "alt text",
    },
    {
      src: "https://storage.googleapis.com/pod_public/1300/197366.jpg",
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
