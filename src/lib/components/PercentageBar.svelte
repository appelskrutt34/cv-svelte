<script>
  export let level = "Advanced";
  export let color = "bg-gray-900";
  export let text;

  let width = level == "Advanced" ? 100 : 60;
</script>

<div class="w-full h-8 text-gray-50 rounded-xl bg-gray-500">
  <div
    class={"h-full rounded-xl bg-gray-900 relative"}
    style={"width:" + width + "%; "}
  >
    <p class="absolute left-2 top-1 font-bold margin-auto">
      {text ?? level}
    </p>
  </div>
</div>
