<script lang="ts">
  import '../styles/fonts.css';
  import bandPhotograph from '../images/tiles.png';
  import EmbeddedVideo from '$lib/components/embedded-video.svelte';
  import Footer from '$lib/components/footer.svelte';
</script>

<main>
  <h1>Your Fearless Leader</h1>
  <img
    alt="Photograph of Your Fearless Leader band members"
    src={bandPhotograph}
  />
  <p>
    We’re a San Francisco based indie rock band known for our dynamic sound and
    intricate orchestral arrangements. Blending powerful vocals with
    contemplative lyrics, we create music that moves between explosive energy
    and haunting stillness. We’re continuing to captivate audiences nationwide
    with our precise arrangements, energizing performances, and unforgettable
    sound.
  </p>
  <EmbeddedVideo />
  <Footer />
</main>

<style>
  :global(body) {
    background-color: rgb(47, 90, 56);
    margin: 0;
  }

  main {
    color: rgb(237, 229, 214);
    font-family: 'NotoSansMono';
    max-width: 600px;
    margin: 48px auto;
    padding: 0 24px;
    text-align: center;
  }

  h1 {
    color: rgb(237, 229, 214);
    font-family: 'LeagueSpartan';
    font-size: 88px;
    margin: 48px 0;
    text-transform: uppercase;

    @media (max-width: 450px) {
      font-size: 54px;
    }
  }

  img {
    height: 600px;
    width: 600px;

    @media (max-width: 648px) {
      height: calc(100vw - 48px);
      width: calc(100vw - 48px);
    }
  }

  p {
    margin: 48px 0;
  }
</style>
