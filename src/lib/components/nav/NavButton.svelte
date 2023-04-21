<script>
  import { fade } from "svelte/transition";

  export let href = "";
  export let text;
  export let showIcon = false;
  export let action;
</script>

<a
  {href}
  aria-label={text}
  class="w-min relative"
  on:mouseenter={() => (showIcon = true)}
  on:mouseleave={() => (showIcon = false)}
  on:click|preventDefault={action}
  >{text}

  {#if showIcon}
    <span
      aria-hidden="true"
      transition:fade
      class="tooltip flex justify-center absolute left-0 right-0 margin-auto"
    >
      <slot />
    </span>
  {/if}
</a>

<style>
  .tooltip {
    top: -0.9em;
  }
</style>
