<script>
  export let image = ''
  export let alt = ''
  export let tooltip = ''
  export let title = ''
  export let description = ''
  export let time = ''
  export let comment = ''
</script>

<div class="rounded overflow-hidden shadow-lg flex flex-col">
  <div class="relative">
    <a href="/">
      <img
        class="w-full h-36"
        src="{image}"
        alt="{alt}"
      />
      <div
        class="hover:bg-transparent transition duration-300 absolute bottom-0 top-0 right-0 left-0 bg-gray-900 opacity-25"
      ></div>
    </a>
    <a href="#!">
      <div
        class="text-xs absolute top-0 right-0 bg-indigo-600 px-4 py-2 text-white mt-3 mr-3 hover:bg-white hover:text-indigo-600 transition duration-500 ease-in-out"
      >
        {tooltip}
      </div>
    </a>
  </div>
  <div class="px-6 py-4 mb-auto">
    <a
      href="/"
      class="font-medium text-lg inline-block hover:text-indigo-600 transition duration-500 ease-in-out mb-2"
      >{title}</a
    >
    <p class="text-gray-500 text-sm">
      {description}.
    </p>
  </div>


  {#if time}
	
  <div class="px-3 py-1 flex flex-row items-center justify-between bg-gray-100">
    <span
      class="py-1 text-xs font-regular text-gray-900 mr-1 flex flex-row items-center"
    >
      <span class="ml-1">{time}</span>
    </span>

    <span
      class="py-1 text-xs font-regular text-gray-900 mr-1 flex flex-row items-center"
    >
      <span class="ml-1">{comment}</span>
    </span>
  </div>
  
  {/if}

</div>
