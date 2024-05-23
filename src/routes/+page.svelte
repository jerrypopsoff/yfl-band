<script lang="ts">
  import '../styles/fonts.css';
  import bandPhotograph from '../images/tiles.png';
  import EmbeddedVideo from '$lib/components/embedded-video.svelte';
  import Footer from '$lib/components/footer.svelte';
  import EmbeddedAudio from '$lib/components/embedded-audio.svelte';
  import { BIO_TEXT } from '$lib/constants';
</script>

<main>
  <h1>Your Fearless Leader</h1>
  <img
    alt="Photograph of Your Fearless Leader band members"
    src={bandPhotograph}
  />
  <p>{BIO_TEXT}</p>
  <EmbeddedVideo />
  <EmbeddedAudio />
  <Footer />
</main>

<style>
  :global(body) {
    background-color: rgb(65, 75, 54);
    margin: 0;

    background: url($lib/images/green_metal_rust_diff_4k.jpg) no-repeat center
      center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
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
