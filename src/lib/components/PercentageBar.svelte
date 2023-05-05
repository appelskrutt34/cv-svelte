<script>
  export let level = "Advanced";
  export let text;

  let width = level == "Advanced" ? 100 : 60;
  let color = "bg-violet-700";
</script>

<div
  class="w-full h-8 text-neutral-50 rounded-xl bg-neutral-900 border-neutral-50 border"
>
  <div
    class={"h-full rounded-xl relative " + color}
    style={"width:" + width + "%; "}
  >
    <p class="absolute left-2 top-1 font-bold margin-auto">
      {text ?? level}
    </p>
  </div>
</div>
