<script>
// @ts-nocheck
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
    export let items = [];
</script>

<Navbar>
    <NavBrand href="/">
      <img src="/logo-flowbite.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Spotify</span>
    </NavBrand>
    <NavHamburger  />
    <NavUl>
      {#each items as item}
        <NavLi href="{item.link}">{item.tag}</NavLi>
      {/each}
    </NavUl>
</Navbar>