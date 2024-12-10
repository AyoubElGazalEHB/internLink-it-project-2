<script>
    // Simuleer een bedrijf profiel (dit kan worden vervangen door dynamische gegevens)
    let company = {
      id: 1,
      name: 'Bedrijf 1',
      image: 'src/images/blank-profile-picture-973460_1280.webp',
      stagePosition: 'Marketing Stage',
      description: 'This is an amazing company that is looking for a talented intern!',
      contact: 'info@bedrijf1.com',
    };
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
  
  <div class="profile-container">
    <div class="profile-content">
      <div class="profile-header">
        <img src={company.image} alt={company.name} class="company-image" />
        <div class="company-info">
          <h2>{company.name}</h2>
          <p>{company.stagePosition}</p>
        </div>
      </div>
  
      <div class="profile-body">
        <h3>About the Company</h3>
        <p>{company.description}</p>
  
        <h3>Contact Information</h3>
        <p>Email: {company.contact}</p>
      </div>
  
      <div class="apply-section">
        <button class="apply-btn">Apply for this Position</button>
      </div>
    </div>
  </div>
  
  <style>
    /* Styling voor de navbar */
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
  
    /* Profile page styles */
    .profile-container {
      font-family: 'Arial', sans-serif;
    }
  
    .profile-header {
      display: flex;
      align-items: center;
      gap: 20px;
      padding: 20px;
      background-color: #f5f5f5;
      border-radius: 8px;
      margin-top: 20px;
    }
  
    .company-image {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      object-fit: cover;
    }
  
    .company-info {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
  
    .company-info h2 {
      margin: 0;
      font-size: 1.5rem;
      color: #333;
    }
  
    .company-info p {
      margin: 0;
      font-size: 1.1rem;
      color: #666;
    }
  
    .profile-body {
      padding: 20px;
      background-color: #fff;
      border-radius: 8px;
      margin-top: 20px;
    }
  
    .profile-body h3 {
      font-size: 1.3rem;
      color: #333;
    }
  
    .profile-body p {
      color: #555;
    }
  
    .apply-section {
      text-align: center;
      margin-top: 20px;
    }
  
    .apply-btn {
      padding: 12px 20px;
      background-color: #007bff;
      color: white;
      font-size: 1.1rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
  
    .apply-btn:hover {
      background-color: #0056b3;
    }
  </style>
  