<script>
    import Card from "../components/Card.svelte";
    const cards = [
      {
        image: "https://images.pexels.com/photos/61180/pexels-photo-61180.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=1&amp;w=500",
        alt: "Image 1",
        tooltip: "Tooltip 1",
        title: "Title 1",
        description: "Description 1",
        time: "Time 1",
        comment: "Comment 1",
      },
      {
        image: "https://images.pexels.com/photos/61180/pexels-photo-61180.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=1&amp;w=500",
        alt: "Image 2",
        tooltip: "Tooltip 2",
        title: "Title 2",
        description: "Description 2",
        time: "Time 2",
        comment: "Comment 2",
      },
      {
        image: "https://images.pexels.com/photos/61180/pexels-photo-61180.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=1&amp;w=500",
        alt: "Image 3",
        tooltip: "Tooltip 3",
        title: "Title 3",
        description: "Description 3",
        time: "Time 3",
        comment: "Comment 3",
      },
    ];
  </script>
  
  <div>
    <div class="max-w-screen-xl mx-auto p-5 sm:p-10 md:p-16">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10">
        {#each cards as card}
          <Card
            image="{card.image}"
            alt="{card.alt}"
            tooltip="{card.tooltip}"
            title="{card.title}"
            description="{card.description}"
            time="{card.time}"
            comment="{card.comment}"
          />
        {/each}
      </div>
    </div>
  </div>