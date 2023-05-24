<script>
  import Api from "$lib/components/icons/Api.svelte";
  import Crow from "$lib/components/icons/Crow.svelte";
  import Worm from "$lib/components/icons/Worm.svelte";
  import Shrimp from "$lib/components/icons/Shrimp.svelte";
  import Kiwi from "$lib/components/icons/Kiwi.svelte";
  import LinkBox from "../LinkBox.svelte";
  import Fish from "../icons/Fish.svelte";
</script>

<section aria-label="Projects" class="flex justify-center text-center flex-col">
  <h1 class="mb-8 text-4xl">PROJECTS</h1>

  <div
    class="grid grid-flow-row grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6"
  >
    <LinkBox
      title="Kryptokrona explorer"
      text="Role: Sveltekit developer"
      tools="# Sveltekit, apexcharts"
      link="https://explorer.kryptokrona.org/"
      ><Shrimp />
    </LinkBox>

    <LinkBox
      title="Kryptokrona api"
      text="Role: Sveltekit developer"
      tools="# Sveltekit, Prometheus, Github api, apexcharts, Docker"
      link="https://xkr.mjovanc.com/monitor"
    >
      <Api />
    </LinkBox>
    <LinkBox
      title="Kryptokrona Kotlin SDK"
      text="Role: Sveltekit developer"
      tools="# Sveltekit, Sveltepress, Docker, Vercel"
      link="https://kryptokrona-kotlin-sdk.vercel.app"
    >
      <Kiwi />
    </LinkBox>

    <LinkBox
      title="Yggdrasil wallet"
      text="Role: Sveltekit developer"
      tools="# Sveltekit, apexcharts"
      link="https://github.com/kryptokrona/yggdrasil-wallet"
    >
      <Fish /></LinkBox
    >

    <LinkBox
      title="Hugin Messenger"
      text="Role: Sveltekit developer"
      tools="# Sveltekit"
      link="https://hugin.chat/"><Worm /></LinkBox
    >

    <LinkBox
      title="Old CV"
      text="Made with react"
      link="https://www.cvebba.com"
      tools="# React"><Crow /></LinkBox
    >
  </div>
</section>
