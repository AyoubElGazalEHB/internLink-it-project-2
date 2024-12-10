<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

{@render children()}
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>InternLink</title>
	<style>
      /* General reset */
      * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
      }

      body {
          font-family: Arial, sans-serif;
          background-color: #f9f9f9;
          color: #333;
      }

      /* Header styles */
      header {
          display: flex;
          justify-content: space-between;
          align-items: center;
          padding: 15px 30px;
          background-color: #fff;
          box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
      }

      .logo {
          font-size: 1.5rem;
          font-weight: bold;
      }

      nav {
          display: flex;
          gap: 20px;
      }

      nav a {
          text-decoration: none;
          color: #333;
          font-size: 1rem;
          transition: color 0.3s ease;
      }

      nav a:hover {
          color: #007bb5;
      }

      .profile {
          display: flex;
          align-items: center;
          gap: 15px;
      }

      .profile-icon {
          width: 35px;
          height: 35px;
          background-color: #ccc;
          border-radius: 50%;
      }

      /* Main section */
      main {
          display: flex;
          align-items: center;
          justify-content: space-between;
          padding: 50px 30px;
      }

      .welcome-section {
          max-width: 50%;
      }

      .welcome-section h1 {
          font-size: 2.5rem;
          margin-bottom: 15px;
      }

      .welcome-section p {
          font-size: 1rem;
          margin-bottom: 20px;
          color: #555;
      }

      .button-container {
          display: flex;
          flex-direction: column;
          gap: 15px;
      }

      button {
          padding: 10px 20px;
          font-size: 1rem;
          font-weight: bold;
          border: none;
          border-radius: 5px;
          cursor: pointer;
          transition: background-color 0.3s ease, transform 0.2s ease;
      }

      .register-btn {
          background-color: #000;
          color: #fff;
      }

      .register-btn:hover {
          background-color: #333;
          transform: scale(1.05);
      }

      .login-btn {
          background-color: #000;
          color: #fff;
      }

      .login-btn:hover {
          background-color: #333;
          transform: scale(1.05);
      }

      /* Placeholder for image section */
      .image-placeholder {
          width: 50%;
          height: 300px;
          background-color: #ddd;
      }
	</style>
</head>
<body>
<header>
	<div class="logo">InternLink</div>
	<nav>
		<a href="#">Discover</a>
		<a href="#">Matches</a>
		<a href="#">Companies</a>
	</nav>
	<div class="profile">
		<div class="profile-icon"></div>
	</div>
</header>
<main>
	<div class="welcome-section">
		<h1>Welcome to InternLink</h1>
		<p>Connect with internship opportunities that match your interests</p>
		<div class="button-container">
			<button class="register-btn">Register</button>
			<button class="login-btn">Login</button>
		</div>
	</div>
	<div class="image-placeholder"></div>
</main>
</body>
</html>
