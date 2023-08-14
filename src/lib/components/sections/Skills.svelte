<script>
  import { tools } from "$lib/data/data.js";
  import CompetenceTable from "$lib/components/CompetenceTable.svelte";
</script>

  <div
    aria-label="Skills"
    class="flex flex-col justify-center text-center"
  >
    <h1 class="mb-8 text-4xl">SKILLS</h1>
    <div class="w-full flex justify-center" style="height: 610px;">
      <div class="w-full md:w-2/3">
        <CompetenceTable data={tools} />
      </div>
    </div>
  </div>

