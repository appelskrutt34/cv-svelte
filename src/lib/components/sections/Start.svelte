<script>
  import PercentageBar from "$lib/components/PercentageBar.svelte";
  import Github from "$lib/components/icons/Github.svelte";
  import Linkedin from "$lib/components/icons/Linkedin.svelte";
</script>

<div aria-label="Home" class="text-neutral-50 flex flex-col md:flex-row">
  <div class="md:w-2/3 flex justify-center lg:justify-end">
    <div class="flex items-center">
      <img
        style="object-position: top;"
        class="rounded-full object-cover border-2 border-white h-60 w-60 sm:mr-10"
        src="./ebbasvensson.jpeg"
        alt="Ebba svensson"
      />
    </div>
  </div>

  <div class="mt-8 md:mt-0 w-full text-center sm:text-left">
    <h1>Name: Ebba Svensson</h1>
    <h2>Role: Web developer</h2>
    <p>From: Sweden</p>
    <p>Age: 28</p>
    <div class="flex mb-8 mt-2 gap-2 justify-center sm:justify-start">
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
    <div class="sm:flex sm:flex-row gap-3 lg:w-4/5">
      <div class="flex flex-col gap-2 text-center w-full">
        <PercentageBar text="C#" level="Advanced" />
        <PercentageBar text="Solidity" level="Advanced" />
        <PercentageBar text="Unity" level="Advanced" />
        <PercentageBar text="Tailwind" level="Advanced" />
        <PercentageBar text="Javascript" level="Advanced" />
      </div>
      <div class="flex flex-col gap-2 text-center w-full mt-2 sm:mt-0">
        <PercentageBar text="Sveltekit" level="Advanced" />
        <PercentageBar text="HTML & CSS" level="Advanced" />
        <PercentageBar text="Responsive design" level="Advanced" />
        <PercentageBar text="WCAG" level="Advanced" />
        <PercentageBar text=".Net" level="Advanced" />
      </div>
    </div>
  </div>
</div>
