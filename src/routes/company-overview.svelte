<script>
  // Mock data for development
  let companies = [
    {
      id: 1,
      name: "Company XYZ",
      tagline: "Innovating the future",
      location: "New York, USA",
    },
    {
      id: 2,
      name: "Tech Solutions",
      tagline: "Building better tech",
      location: "San Francisco, USA",
    },
  ];
</script>

<main class="p-6">
  <h1 class="text-4xl font-bold mb-6">Company Overview</h1>
  <section class="grid grid-cols-1 sm:grid-cols-2 gap-6">
    {#each companies as company}
      <div class="border p-4 rounded shadow-md hover:shadow-lg">
        <h2 class="text-2xl font-semibold">{company.name}</h2>
        <p class="text-lg text-gray-600">{company.tagline}</p>
        <p class="text-sm text-gray-500">Location: {company.location}</p>
        <a href={`/company-profile/${company.id}`} class="text-blue-600 hover:underline mt-2 block">View Profile</a>
      </div>
    {/each}
  </section>
</main>

<style>
  main {
    font-family: Arial, sans-serif;
  }
</style>
