<script>
  let firstName = '';
  let lastName = '';
  let bio = '';
  let currentStudy = '';
  let resumeFile = null;
  const interestsOptions = ['Python', 'Data Engineering', 'Machine Learning', 'Web Development'];

  const handleFileUpload = (event) => {
    resumeFile = event.target.files[0];
  };

  const saveChanges = () => {
    console.log('Saving changes...');
  };
</script>

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
    gap: 15px;
  }

  .navbar .nav-items img {
    border-radius: 50%;
    width: 40px;
    height: 40px;
    margin-left: 10px;
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
    gap: 10px;
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
    background-color: #4c77af;
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
    text-align: center;
    margin-bottom: 20px;
  }

  .profile-header img {
    border-radius: 50%;
    width: 100px;
    height: 100px;
    margin-bottom: 10px;
  }

  .profile-header button {
    margin-top: 10px;
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  .profile-header button:hover {
    background-color: #4c77af;
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
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
    margin-bottom: 20px;
  }
</style>

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
      <img src="src/images/blank-profile-picture-973460_1280.webp" alt="Profile Picture" />
      <h2>Jonh Doe</h2>
      <button>Change Profile Picture</button>
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

      <label>Interests</label>
      <div class="dropdown">
        {#each interestsOptions as interest}
          <div>{interest}</div>
        {/each}
      </div>

      <button type="submit" class="button">Save Changes</button>
    </form>
  </div>
</div>
