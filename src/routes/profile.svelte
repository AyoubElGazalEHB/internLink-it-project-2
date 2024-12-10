<script>
    let firstName = '';
    let lastName = '';
    let bio = '';
    let currentStudy = '';
    let resumeFile = null;
    const interestsOptions = ['Python', 'Data Engineering', 'Machine Learning', 'Web Development'];
    let selectedInterest = '';
  
    const handleFileUpload = (event) => {
      resumeFile = event.target.files[0];
    };
  
    const saveChanges = () => {
      console.log('Saving changes...');
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
  
  <!-- Page Layout -->
  <div class="page-container">
    <!-- Sidebar -->
    <div class="sidebar">
      <button>Edit Profile</button>
      <button>Account</button>
      <button>Notifications</button>
    </div>
  
    <!-- Main Content -->
    <div class="main-content">
      <div class="profile-header">
        <div class="profile-container">
          <img src="src/images/blank-profile-picture-973460_1280.webp" alt="Profile Picture" />
          <div>
            <h2 class="profile-name">John Doe</h2>
            <button class="change-profile-btn">Change Profile Picture</button>
          </div>
        </div>
      </div>
  
      <form on:submit|preventDefault={saveChanges}>
        <input type="text" class="input-field" placeholder="First Name" bind:value={firstName} />
        <input type="text" class="input-field" placeholder="Last Name" bind:value={lastName} />
        <textarea class="input-field" placeholder="Write a short bio about yourself" bind:value={bio}></textarea>
        <input type="text" class="input-field" placeholder="Current Study" bind:value={currentStudy} />
  
        <div class="file-upload">
          <label for="resume-upload">Upload Resume</label>
          <input id="resume-upload" type="file" on:change={handleFileUpload} />
        </div>
  
        <label for="interests-dropdown">Interests</label>
        <select id="interests-dropdown" class="dropdown" bind:value={selectedInterest}>
          <option value="" disabled selected>Select your interest</option>
          {#each interestsOptions as interest}
            <option value={interest}>{interest}</option>
          {/each}
        </select>
  
        <button type="submit" class="save-button">Save Changes</button>
      </form>
    </div>
  </div>
  
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
  
    body {
      font-family: Arial, sans-serif;
      background-color: #f7f7f7;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }
  
    /* Navbar */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 20px;
      background-color: #ffffff;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      margin-bottom: 20px; /* Meer spatie tussen navbar en content */
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
      gap: 20px; /* Spatie tussen de knoppen */
    }
  
    .navbar .nav-items img {
      border-radius: 50%;
      width: 40px;
      height: 40px;
    }
  
    /* Page Layout */
    .page-container {
      display: flex;
      flex: 1;
    }
  
    /* Sidebar */
    .sidebar {
      width: 200px;
      background-color: #ffffff;
      border-right: 1px solid #ddd;
      box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
      padding: 20px;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
  
    .sidebar button {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      text-align: left;
      cursor: pointer;
      transition: background-color 0.3s;
    }
  
    .sidebar button:hover {
      background-color: #45a049;
    }
  
    /* Main Content */
    .main-content {
      flex: 1;
      padding: 20px;
      background-color: #ffffff;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }
  
    .profile-header {
      margin-bottom: 20px;
    }
  
    .profile-container {
      display: flex;
      align-items: center;
      gap: 20px;
    }
  
    .profile-container img {
      border-radius: 50%;
      width: 100px;
      height: 100px;
    }
  
    .profile-name {
      font-size: 1.8em;
      font-weight: bold;
    }
  
    .change-profile-btn {
      margin-top: 5px;
      padding: 8px 15px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 0.9em;
    }
  
    .change-profile-btn:hover {
      background-color: #45a049;
    }
  
    .input-field,
    .file-upload input {
      width: 100%;
      padding: 12px;
      border: 1px solid #ddd;
      border-radius: 8px;
      margin-bottom: 20px;
      font-size: 1em;
      background-color: #f9f9f9;
    }
  
    .dropdown {
      width: 100%;
      padding: 12px;
      border: 1px solid #ddd;
      border-radius: 8px;
      background-color: #f9f9f9;
      font-size: 1em;
      margin-bottom: 20px;
    }
  
    .save-button {
      padding: 10px 20px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 1em;
      cursor: pointer;
    }
  
    .save-button:hover {
      background-color: #45a049;
    }
  </style>
  