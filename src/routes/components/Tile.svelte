
<script>
// @ts-nocheck

  export let title
  export let description
  export let image
  export let background
  
</script>

<div class="flex flex-col {background} rounded-lg items-center p-3">
  <div>
    <img src="{image}" alt="svelte" class="h-20 w-20">
  </div>
  <div class="flex flex-col my-3 w-full items-center">
    <div>
      <span class="font-bold text-white">{title}</span>
    </div>
    <div>
      <span class="text-white">{description}</span>
    </div>
  </div>
</div>