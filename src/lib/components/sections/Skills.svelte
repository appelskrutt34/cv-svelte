<script>
  import { tools } from "$lib/data/data.js";
  import CompetenceTable from "$lib/components/CompetenceTable.svelte";
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";
  onMount(() => {
    draw = true;
  });

  let draw = false;
</script>

{#if draw}
  <section
    in:fade
    aria-label="Skills"
    class="flex flex-col justify-center text-center"
  >
    <h1 class="mb-8 text-4xl">SKILLS</h1>
    <div class="w-full flex justify-center" style="height: 610px;">
      <div class="w-full md:w-2/3">
        <CompetenceTable data={tools} />
      </div>
    </div>
  </section>
{/if}
