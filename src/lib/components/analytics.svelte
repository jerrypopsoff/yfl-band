<script lang="ts">
  import { dev } from '$app/environment';
  const GTAG_MEASUREMENT_ID = 'G-H74S4LHGS3';
</script>

<svelte:head>
  {#if !dev}
    <script
      async
      src={`https://www.googletagmanager.com/gtag/js?id=${GTAG_MEASUREMENT_ID}`}
    ></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag() {
        dataLayer.push(arguments);
      }
      gtag('js', new Date());
      gtag('config', GTAG_MEASUREMENT_ID);
    </script>
  {/if}
</svelte:head>
