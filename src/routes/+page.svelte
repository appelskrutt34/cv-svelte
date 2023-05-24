<script>
  import Education from "../lib/components/sections/Education.svelte";
  import Projects from "../lib/components/sections/Projects.svelte";
  import Start from "../lib/components/sections/Start.svelte";
  import Work from "../lib/components/sections/Work.svelte";
</script>

<div class="py-32 md:py-48 flex justify-center bg-neutral-900 w-full" id="home">
  <div class="container px-4">
    <Start />
  </div>
</div>

<div class="container py-32 md:py-40 px-4" id="projects">
  <Projects />
</div>

<div
  class="py-32 md:py-40 w-full bg-neutral-900 flex justify-center"
  id="education"
>
  <div class="container px-4">
    <Education />
  </div>
</div>

<div class="container py-32 md:py-40 px-4" id="work">
  <Work />
</div>
