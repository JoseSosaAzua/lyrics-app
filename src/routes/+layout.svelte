<script>
import NavBar from './components/NavBar.svelte';
import "../app.pcss";

let items = [{
        tag: "Inicio",
        link: "/home"
    },
    {
        tag: "Letras",
        link: "/lyrics"
    },
    {
        tag: "Karaoke",
        link: "/karaoke"
    },
    {
        tag: "Mas",
        link: "/more"
    },
];
</script>

<div class="flex flex-col h-screen">
  <!-- Encabezado -->
  <header class="bg-blue-500 text-white py-4">
    <NavBar {items} />
  </header>

  <!-- Sección central dividida en dos partes -->
  <main class="flex-1 flex">
    <section class="w-1/2 bg-gray-200 flex justify-center items-center">
      <h2 class="text-center py-8 text-lg font-semibold">Sección 1</h2>
    </section>
    <section class="w-1/2 bg-gray-300 flex justify-center items-center">
      <h2 class="text-center py-8 text-lg font-semibold">Sección 2</h2>
    </section>
  </main>

  <!-- Pie de página -->
  <footer class="bg-blue-500 text-white py-4">
    <h3 class="text-center text-sm">Footer</h3>
  </footer>
</div>

