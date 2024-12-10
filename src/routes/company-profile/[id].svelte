<script>
  // Mock data for development
  let company = {
    name: "Company XYZ",
    tagline: "Innovating the future",
    location: "New York, USA",
    industry: "Technology",
    website: "www.companyxyz.com",
    representatives: [
      { name: "John Doe", role: "CEO" },
      { name: "Jane Smith", role: "Head of Marketing" },
    ],
  };
</script>

<!-- The rest of the page remains the same -->
<main class="p-6">
  <section class="bg-gray-200 text-center py-12">
    <h1 class="text-4xl font-bold">{company.name}</h1>
    <p class="text-xl mt-4">{company.tagline}</p>
  </section>
  <!-- Continue with the dynamic UI -->
</main>

<script>
  // Access the dynamic ID parameter from the route
  export let params;
  const { id } = params;
</script>

<h1>Company Profile</h1>
<p>This page is for company ID: {id}</p>
