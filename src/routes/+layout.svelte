<script>
  import "../app.css";
  import Nav from "$lib/components/nav/Nav.svelte";
</script>

<div class="w-full bg-gray-50 text-gray-900 font-base">
  <Nav />
  <main class="w-full flex items-center flex-col">
    <slot />
  </main>
</div>
