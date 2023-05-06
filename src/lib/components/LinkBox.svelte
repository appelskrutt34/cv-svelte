<script>
  export let title;
  export let text;
  export let link;
  export let tools;
</script>

<a
  target="_blank"
  href={link}
  aria-label={title}
  class="p-8 border border-neutral-900 rounded-lg hover:shadow-lg hover:shadow-neutral-500/50 text-left transition ease-in-out duration-400"
>
  <slot />
  <h2 class="mt-4">{title}</h2>
  <p>{text}</p>
  <p class="mt-2 text-neutral-400">{tools}</p>
</a>
