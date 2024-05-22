<script>
  import MediaQuery from 'svelte-media-queries';
</script>

<MediaQuery query="(max-width: 648px)" let:matches>
  <iframe
    width={matches ? 320 : 600}
    height={matches ? 180 : 337.5}
    src="https://www.youtube.com/embed/cqLAp-eYSao?si=pQZYxpQ_5S4l7NrD"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen
  ></iframe>
</MediaQuery>
