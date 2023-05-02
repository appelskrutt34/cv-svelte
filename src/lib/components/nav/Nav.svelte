<script>
  import Heart from "$lib/components/icons/Heart.svelte";
  import Medal from "../icons/Medal.svelte";
  import Portfolio from "../icons/Portfolio.svelte";
  import NavButton from "./NavButton.svelte";
  import Fire from "../icons/Fire.svelte";
  import Burger from "../icons/Burger.svelte";
  import { fly } from "svelte/transition";
  import XMark from "../icons/XMark.svelte";

  let openMenu = false;

  function scrollIntoView(e, top = false) {
    const el = document.querySelector(e.target.getAttribute("href"));
    if (!el) return;
    el.scrollIntoView({
      block: top ? "start" : "center",
      behavior: "smooth",
    });
    openMenu = false;
  }
</script>

<nav
  class="w-full flex justify-center fixed top-0 md:backdrop-blur-xl md:bg-gray-50/50 z-50"
  aria-label="Main navigation"
>
  <div class="justify-center gap-16 container hidden md:flex px-4 py-6">
    <NavButton href="#home" text="Home" action={scrollIntoView}>
      <Heart />
    </NavButton>
    <NavButton href="#projects" text="Projects" action={scrollIntoView}>
      <Fire />
    </NavButton>
    <NavButton href="#education" text="Education" action={scrollIntoView}>
      <Medal />
    </NavButton>
    <NavButton href="#work" text="Work" action={scrollIntoView}>
      <Portfolio />
    </NavButton>
  </div>

  <div class="md:hidden w-full">
    <div
      class="backdrop-blur-xl bg-gray-50/50 w-full flex justify-end items-end px-4 py-6"
    >
      <button
        on:click={() => {
          openMenu = !openMenu;
        }}
      >
        {#if openMenu} <XMark /> {:else} <Burger /> {/if}
      </button>
    </div>

    {#if openMenu}
      <div
        in:fly={{ y: -10, duration: 300 }}
        out:fly={{ y: -10, duration: 300 }}
        class="w-full backdrop-blur-xl bg-gray-50/50 text-center py-4 flex flex-col gap-4"
      >
        <a
          href="#home"
          on:click|preventDefault={(e) => {
            scrollIntoView(e, true);
          }}>Home</a
        >
        <a
          href="#projects"
          on:click|preventDefault={(e) => {
            scrollIntoView(e, true);
          }}>Projects</a
        >
        <a
          href="#education"
          on:click|preventDefault={(e) => {
            scrollIntoView(e, true);
          }}>Education</a
        >
        <a
          href="#work"
          on:click|preventDefault={(e) => {
            scrollIntoView(e, true);
          }}>Work history</a
        >
      </div>
    {/if}
  </div>
</nav>
