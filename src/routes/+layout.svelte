<script>
  
	import NavBar from './components/NavBar.svelte';
  import "../app.pcss";

  let items = [
    {tag: "Inicio", link: "/home"},
    {tag: "Letras", link: "/lyrics"},
    {tag: "Karaoke", link: "/karaoke"},
    {tag: "Mas", link: "/more"},
  ];

</script>

<NavBar items={items}/>

<slot />
