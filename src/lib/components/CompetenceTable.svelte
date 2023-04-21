<script>
  import PercentageBar from "./PercentageBar.svelte";
  import Search from "./icons/Search.svelte";
  export let data = [];

  let searchInput = "";

  $: filtered = data.filter((d) =>
    d.name.toLowerCase().includes(searchInput.toLowerCase())
  );
</script>

<div class="relative text-gray-900">
  <div class="search-icon">
    <Search />
  </div>

  <input
    bind:value={searchInput}
    class="search-input rounded-md w-full border-gray-900 border focus:outline focus:outline-gray-900"
    type="text"
    aria-label="search for skill"
    placeholder="search"
  />
</div>

<div class="rounded-md border border-gray-900 w-full mt-4">
  <div
    class={(filtered.length > 0 ? "border-b " : "") +
      "table-grid p-2 border-gray-900 px-4 "}
  >
    <h3 class="text-left w-full">Skill</h3>
    <h3 class="text-center w-full">Level</h3>
  </div>

  <div
    class="px-4 focus:outline focus:outline-gray-900"
    style="max-height: 500px; overflow-y: scroll; "
  >
    {#each filtered as item, i}
      <div
        class={(i == filtered.length - 1
          ? "border-none "
          : i == 0
          ? "mt-2 "
          : "") + "table-grid w-full border-b p-2  border-gray-900 "}
      >
        <div class="items-center w-full flex">
          <p class="text-left w-full">{item.name}</p>
        </div>

        <div class="px-6 md:px-12">
          <PercentageBar level={item.competence} />
        </div>
      </div>
    {/each}
  </div>
</div>

<style>
  .search-icon {
    display: flex;
    align-items: center;
    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    padding-left: 0.5rem;
  }
  .search-input {
    padding-left: 2.5rem;
    padding-bottom: 0.5rem;
    padding-top: 0.5rem;
  }

  .table-grid {
    display: grid;
    grid-template-columns: 35% 65%;
  }
</style>
