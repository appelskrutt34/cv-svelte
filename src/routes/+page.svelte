<script>
  import Education from "../lib/components/sections/Education.svelte";
  import Projects from "../lib/components/sections/Projects.svelte";
  import Start from "../lib/components/sections/Start.svelte";
  import Work from "../lib/components/sections/Work.svelte";
</script>

<div
  class="container flex justify-center items-center px-4 pt-32 sm:pt-0"
  id="home"
  style="min-height:100vh"
>
  <Start />
</div>

<div class="container pt-40 px-4" id="projects">
  <Projects />
</div>

<div
  class="mt-40 py-40 w-full px-4 bg-gray-900 flex justify-center"
  id="education"
>
  <Education />
</div>

<div class="container pt-40 px-4" id="work">
  <Work />
</div>

<div class="mt-40" />
