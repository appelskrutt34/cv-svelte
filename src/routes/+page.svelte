<script>
  import Education from "../lib/components/sections/Education.svelte";
  import Projects from "../lib/components/sections/Projects.svelte";
  import Start from "../lib/components/sections/Start.svelte";
  import Work from "../lib/components/sections/Work.svelte";
</script>

<div
  class="container flex justify-center items-center px-4 mt-20 sm:mt-0"
  style="min-height:100vh"
>
  <Start />
</div>

<div class="container mt-40 px-4">
  <Projects />
</div>

<div class="mt-40 py-40 w-full px-4 bg-gray-900 flex justify-center">
  <Education />
</div>

<div class="container mt-40 px-4">
  <Work />
</div>

<div class="mt-40" />
