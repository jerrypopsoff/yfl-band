<script lang="ts">
  import '../styles/fonts.css';
  import bandPhotograph from '$lib/images/yfl-profile-photograph.png';
  import bandPhotographWebp from '$lib/images/yfl-profile-photograph.webp';
  import EmbeddedVideo from '$lib/components/embedded-video.svelte';
  import Footer from '$lib/components/footer.svelte';
  import EmbeddedAudio from '$lib/components/embedded-audio.svelte';
  import { BIO_TEXT } from '$lib/constants';
  import Analytics from '$lib/components/analytics.svelte';
</script>

<Analytics />

<main>
  <h1>Your Fearless Leader</h1>
  <picture>
    <source type="image/webp" srcset={bandPhotographWebp} />
    <img
      alt="Photograph of Your Fearless Leader band members"
      src={bandPhotograph}
    />
  </picture>
  <p>{BIO_TEXT}</p>
  <EmbeddedVideo />
  <EmbeddedAudio />
  <Footer />
</main>

<style>
  :global(body) {
    background-color: rgb(66, 76, 55);
    margin: 0;

    background-image: url($lib/images/green-metal-rust-texture.jpg);
    background-image: image-set(
      url($lib/images/green-metal-rust-texture.webp),
      url($lib/images/green-metal-rust-texture.jpg)
    );
    background-image: -webkit-image-set(
      url($lib/images/green-metal-rust-texture.webp),
      url($lib/images/green-metal-rust-texture.jpg)
    );

    background-attachment: fixed;
    background-position: center center;
    background-repeat: no-repeat;

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
