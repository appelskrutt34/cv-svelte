<script>
  export let href = "";
  export let text;
  export let action;
</script>

<a
  {href}
  aria-label={text}
  class="w-min relative group transition duration-200 hover:text-neutral-400"
  on:click|preventDefault={action}
  >{text}

  <span
    class="block opacity-0 group-hover:opacity-100 transition-all duration-200 h-0.5 bg-violet-700"
  />
</a>
