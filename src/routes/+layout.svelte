<script>
  import "../app.css";
  import Nav from "$lib/components/nav/Nav.svelte";
</script>

<div class="w-full bg-neutral-100 text-neutral-900 font-base">
  <Nav />
  <main class="w-full flex items-center flex-col">
    <slot />
  </main>
</div>
