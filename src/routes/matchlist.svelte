<script>
    // Bedrijfgegevens
    let pendingCompanies = [
      { id: 1, name: 'Bedrijf 1', image: 'src/images/blank-profile-picture-973460_1280.webp', stagePosition: 'Marketing Stage' },
      { id: 2, name: 'Bedrijf 2', image: 'src/images/blank-profile-picture-973460_1280.webp', stagePosition: 'Software Engineer Intern' },
    ];
  
    let matchCompanies = [
      { id: 3, name: 'Bedrijf 3', image: 'src/images/blank-profile-picture-973460_1280.webp', stagePosition: 'Design Stage' },
      { id: 4, name: 'Bedrijf 4', image: 'src/images/blank-profile-picture-973460_1280.webp', stagePosition: 'Data Scientist Intern' },
    ];
  
    function viewApplication(companyId) {
      // Dit kan de student doorverwijzen naar de profielpagina van het bedrijf
      alert(`Bekijk sollicitatie voor bedrijf ${companyId}`);
    }
  </script>
  
  <!-- Navbar -->
  <div class="navbar">
    <div class="logo-container">
      <img src="src/images/blank-profile-picture-973460_1280.webp" alt="Logo" />
      <div class="logo-text">InternLink</div>
    </div>
    <div class="nav-items">
      <span>Discover</span>
      <span>Matches</span>
      <span>Companies</span>
      <img src="src/images/blank-profile-picture-973460_1280.webp" alt="User" />
    </div>
  </div>
  
  <!-- Container with Pending and Match List -->
  <div class="container">
    <!-- Pending List -->
    <div class="list-section">
      <h2>Pending</h2>
      <div class="companies">
        {#each pendingCompanies as company}
          <div class="company-item" key={company.id}>
            <img src={company.image} alt={company.name} class="company-image" />
            <div class="company-info">
              <h3>{company.name}</h3>
              <p>{company.stagePosition}</p>
              <button on:click={() => viewApplication(company.id)} class="view-btn">View Application</button>
            </div>
          </div>
        {/each}
      </div>
    </div>
  
    <!-- Matchlist -->
    <div class="list-section">
      <h2>Matchlist</h2>
      <div class="companies">
        {#each matchCompanies as company}
          <div class="company-item" key={company.id}>
            <img src={company.image} alt={company.name} class="company-image" />
            <div class="company-info">
              <h3>{company.name}</h3>
              <p>{company.stagePosition}</p>
              <button on:click={() => viewApplication(company.id)} class="view-btn">View Application</button>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
  
  <style>
    /* Navbar Styling */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 20px;
      background-color: #ffffff;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      margin-bottom: 20px;
    }
  
    .navbar .logo-container {
      display: flex;
      align-items: center;
      gap: 10px;
    }
  
    .navbar .logo-container img {
      width: 40px;
      height: 40px;
      object-fit: contain;
    }
  
    .navbar .logo-container .logo-text {
      font-size: 1.5em;
      font-weight: bold;
      color: #4CAF50;
    }
  
    .navbar .nav-items {
      display: flex;
      align-items: center;
      gap: 20px;
    }
  
    .navbar .nav-items img {
      border-radius: 50%;
      width: 40px;
      height: 40px;
    }
  
    /* General container styling */
    .container {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      padding: 20px;
      background-color: #f5f5f5;
      min-height: 100vh;
      font-family: 'Arial', sans-serif;
    }
  
    .list-section {
      width: 48%;
      background-color: #fff;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
  
    h2 {
      text-align: center;
      font-size: 1.5rem;
      margin-bottom: 20px;
      color: #333;
    }
  
    /* Company item styling */
    .companies {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
  
    .company-item {
      display: flex;
      align-items: center;
      gap: 15px;
      padding: 15px;
      border-radius: 8px;
      background-color: #f9f9f9;
      transition: transform 0.2s ease-in-out, background-color 0.3s ease;
    }
  
    .company-item:hover {
      transform: translateY(-5px);
      background-color: #e8f7f3;
    }
  
    .company-image {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      object-fit: cover;
    }
  
    .company-info {
      display: flex;
      flex-direction: column;
      gap: 5px;
    }
  
    .company-info h3 {
      font-size: 1.1rem;
      color: #333;
      margin: 0;
    }
  
    .company-info p {
      font-size: 0.9rem;
      color: #555;
      margin: 0;
    }
  
    .view-btn {
      margin-top: 10px;
      padding: 8px 15px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.2s;
    }
  
    .view-btn:hover {
      background-color: #0056b3;
    }
  </style>
  