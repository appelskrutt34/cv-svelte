<script>
  import Code from "../icons/Code.svelte";
  import Unity from "../icons/Unity.svelte";
  import Ethereum from "../icons/Ethereum.svelte";
  import Socks from "../icons/Socks.svelte";
  import Book from "../icons/Book.svelte";
</script>

<section
  aria-label="Education"
  class="flex justify-center text-center flex-col text-neutral-50 container"
>
  <h1 class="mb-8 text-4xl">EDUCATION</h1>
  <div class="grid grid-flow-row grid-cols-1 md:grid-cols-3 gap-6">
    <div
      class="p-4 border bg-neutral-50 text-neutral-900 rounded-lg hover:shadow-lg flex justify-center items-center flex-col h-60"
    >
      <Code />
      <h2 class="mt-4">Software development and Mobile apps</h2>
      <p>Bachelor's degree at Jönköping university</p>
    </div>

    <div
      class="p-8 border bg-neutral-50 text-neutral-900 rounded-lg flex justify-center items-center flex-col h-60"
    >
      <Unity />

      <h2 class="mt-4">Technology and Game development</h2>
      <p>Senior high school</p>
    </div>

    <div
      class="p-8 border bg-neutral-50 text-neutral-900 rounded-lg flex justify-center items-center flex-col h-60"
    >
      <Ethereum />

      <h2 class="mt-4">Smart contract programming</h2>
      <p>Moralis academy</p>
    </div>

    <div
      class="p-8 border bg-neutral-50 text-neutral-900 rounded-lg flex justify-center items-center flex-col h-60"
    >
      <Socks />
      <h2 class="mt-4">Millitary training</h2>
      <p>P4 skövde</p>
    </div>

    <div
      class="p-8 border bg-neutral-50 text-neutral-900 rounded-lg flex justify-center items-center flex-col h-60"
    >
      <Book />
      <h2 class="mt-4">Russian language</h2>
      <p>Dalarnas högskola</p>
    </div>
  </div>
</section>
