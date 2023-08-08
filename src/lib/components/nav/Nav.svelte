<script>
  import NavButton from "./NavButton.svelte";
  import Burger from "../icons/Burger.svelte";
  import { fly, slide } from "svelte/transition";
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
  class="text-neutral-50 w-full flex justify-center fixed top-0 md:backdrop-blur-xl md:bg-neutral-900/50 z-50 md:border-b md:border-neutral-800"
  aria-label="Main navigation"
>
  <div class="justify-center gap-16 container hidden md:flex px-4 py-6">
    <NavButton href="#home" text="Home" action={scrollIntoView}>
    </NavButton>
    <NavButton href="#projects" text="Projects" action={scrollIntoView}>
    </NavButton>
    <NavButton href="#education" text="Education" action={scrollIntoView}>
    </NavButton>
    <NavButton href="#work" text="Work" action={scrollIntoView}>
    </NavButton>
  </div>

  <div class="md:hidden w-full">
    <div
      class="bg-neutral-900 w-full flex justify-end items-end px-4 py-6 border-b border-neutral-800"
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
        in:slide={{ y: -10, duration: 300 }}
        out:slide={{ y: -10, duration: 300 }}
        class="w-full bg-neutral-900 text-center py-4 flex flex-col gap-4 border-b border-neutral-800"
        style="margin-top: -2px"
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
