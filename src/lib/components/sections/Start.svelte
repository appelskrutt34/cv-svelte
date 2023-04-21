<script>
  import { fade } from "svelte/transition";
  import PercentageBar from "$lib/components/PercentageBar.svelte";
  import Github from "$lib/components/icons/Github.svelte";
  import Linkedin from "$lib/components/icons/Linkedin.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    draw = true;
  });

  let draw = false;
  let image;
</script>

{#if draw}
  <section
    aria-label="Home"
    in:fade={{ duration: 800 }}
    class="flex flex-col md:flex-row gap-6 justify-center items-center w-full"
  >
    <img
      bind:this={image}
      in:fade={{ duration: 800 }}
      on:load={() => {
        image.classList.add("opacity-one");
      }}
      class="opacity-zero transition-opacity ease-in duration-400 max-h-96 sm:px-10"
      src="./111.png"
      alt="Avatar"
    />
    <div class="w-full mt-2 sm:mt-0">
      <h1>Name: Ebba Svensson</h1>
      <h2 class="mb-1">Role: Web developer</h2>
      <p>From: Sweden</p>
      <p>Age: 27</p>
      <div class="flex mt-4 mb-4 gap-2">
        <a
          href="https://github.com/appelskrutt34"
          aria-label="Github"
          target="_blank"><Github /></a
        >
        <a
          href="https://www.linkedin.com/in/ebba-svensson-6a295b187/"
          aria-label="Linkedin"
          target="_blank"><Linkedin /></a
        >
      </div>
      <div
        class="md:flex md:flex-row gap-1 justify-center h-full w-full"
        style="max-width: 550px;"
      >
        <div class="flex flex-col gap-1 text-center w-full">
          <PercentageBar text="C#" level="Advanced" />
          <PercentageBar text="Solidity" level="Intermediate" />
          <PercentageBar text="ASP.Net MVC" level="Advanced" />
          <PercentageBar text="Unity" level="Intermediate" />
          <PercentageBar text="Azure DevOps" level="Intermediate" />
          <PercentageBar text="Javascript" level="Advanced" />
        </div>
        <div class="flex flex-col gap-1 text-center w-full mt-2 md:mt-0">
          <PercentageBar text="Tailwind" level="Advanced" />
          <PercentageBar text="Sveltekit" level="Advanced" />
          <PercentageBar text="HTML & CSS" level="Advanced" />
          <PercentageBar text="Responsive design" level="Advanced" />
          <PercentageBar text="WCAG" level="Advanced" />
          <PercentageBar text="React" level="Intermediate" />
        </div>
      </div>
    </div>
  </section>
{/if}
