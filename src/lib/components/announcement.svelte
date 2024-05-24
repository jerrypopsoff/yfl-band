<script>
  import {
    ANNOUNCEMENT_ACTION_TEXT,
    ANNOUNCEMENT_TEXT,
    ANNOUNCEMENT_URL,
  } from '$lib/constants';
  import { fly } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';

  let hasBeenDismissed = false;
  let hasBannerAction = Boolean(ANNOUNCEMENT_ACTION_TEXT && ANNOUNCEMENT_URL);

  function dismiss() {
    hasBeenDismissed = true;
  }
</script>

{#if ANNOUNCEMENT_TEXT && !hasBeenDismissed}
  <div
    transition:fly={{
      delay: 150,
      duration: 300,
      x: 100,
      y: 500,
      opacity: 0.5,
      easing: quintOut,
    }}
  >
    <button aria-label="close" on:click={dismiss}>✕</button>
    <span
      class={hasBannerAction ? 'content' : 'content content--without-action'}
    >
      {ANNOUNCEMENT_TEXT}
    </span>
    {#if hasBannerAction}
      <a href={ANNOUNCEMENT_URL} rel="noreferrer" target="_blank">
        {ANNOUNCEMENT_ACTION_TEXT}
      </a>
    {/if}
  </div>
{/if}

<style>
  div {
    background-color: rgb(237, 229, 214);
    color: #212121;

    position: fixed;
    bottom: 24px;
    right: 24px;

    display: flex;
    flex-direction: column;
    align-items: center;
    width: 350px;

    @media (max-width: 500px) {
      width: auto;
      left: 24px;
    }
  }

  button {
    background-color: rgb(237, 229, 214);
    color: #212121;

    align-self: flex-end;
    border: none;
    cursor: pointer;
    font-family: sans-serif;
    padding: 24px 24px 16px;
  }

  .content {
    margin: 0 24px 4px;
  }

  .content--without-action {
    margin: 0 24px 24px;
  }

  a {
    color: #212121;
    display: flex;
    margin-bottom: 12px;
    padding: 8px 12px;
  }
</style>
