<script>
  // Mock data for development
  let companies = [
    { id: 1, name: "Company XYZ" },
    { id: 2, name: "Dexerto" },
    { id: 3, name: "Tech Innovators" },
    { id: 4, name: "Startup Central" },
  ];
</script>

<!-- The rest of the page remains the same -->
<main class="p-6">
  <h1 class="text-4xl font-bold mb-6">Attending Companies</h1>
  <p class="mb-8">Explore the amazing companies that are attending the event.</p>

  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
    {#each companies as company}
      <div class="p-4 bg-gray-100 rounded-lg shadow-md text-center">
        <p class="font-semibold">{company.name}</p>
      </div>
    {/each}
  </div>
</main>
