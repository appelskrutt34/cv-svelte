<script>
  import Api from "$lib/components/icons/Api.svelte";
  import Bars from "$lib/components/icons/Bars.svelte";
  import Chat from "$lib/components/icons/Chat.svelte";
  import Profile from "$lib/components/icons/Profile.svelte";
  import Wallet from "$lib/components/icons/Wallet.svelte";
</script>

<section aria-label="Projects" class="flex justify-center text-center flex-col">
  <h1 class="mb-8 text-4xl">PROJECTS</h1>

  <div class="grid grid-flow-row grid-cols-1 sm:grid-cols-3 gap-6">
    <a
      target="_blank"
      href="https://xkr.mjovanc.com/monitor"
      aria-label="Kryptokrona api"
      class="p-8 border border-gray-900 rounded-lg hover:shadow-lg hover:shadow-gray-500/50 flex justify-center items-center flex-col transition ease-in-out duration-400 h-60"
    >
      <Api />
      <h2>Kryptokrona api</h2>
      <p>Role: Solo Sveltekit developer</p>
    </a>

    <a
      target="_blank"
      href="https://explorer.kryptokrona.org/"
      aria-label="Kryptokrona explorer"
      class="p-8 border bg-gray-900 text-gray-50 rounded-lg hover:shadow-lg hover:shadow-gray-500/50 flex justify-center items-center flex-col transition ease-in-out duration-400 h-60"
    >
      <Bars />
      <h2>Kryptokrona explorer</h2>
      <p>Role: Sveltekit developer</p>
    </a>

    <a
      target="_blank"
      href="https://github.com/kryptokrona/yggdrasil-wallet"
      aria-label="Yggdrasil wallet"
      class="p-8 border border-gray-900 rounded-lg hover:shadow-lg hover:shadow-gray-500/50 flex justify-center items-center flex-col transition ease-in-out duration-400 h-60"
    >
      <Wallet />
      <h2>Yggdrasil wallet</h2>
      <p>Role: Sveltekit developer</p>
    </a>

    <a
      target="_blank"
      href="https://hugin.chat/"
      aria-label="Hugin"
      class="p-8 border bg-gray-900 text-gray-50 rounded-lg hover:shadow-lg hover:shadow-gray-500/50 flex justify-center items-center flex-col transition ease-in-out duration-400 h-60"
    >
      <Chat />

      <h2>Hugin messenger</h2>
      <p>Role: Sveltekit developer</p>
    </a>

    <a
      target="_blank"
      href="https://www.cvebba.com"
      aria-label="cv"
      class="p-8 border border-gray-900 rounded-lg hover:shadow-lg hover:shadow-gray-500/50 flex justify-center items-center flex-col transition ease-in-out duration-400 h-60"
    >
      <Profile />

      <h2>Old CV</h2>
      <p>Made with React</p>
    </a>
  </div>
</section>
