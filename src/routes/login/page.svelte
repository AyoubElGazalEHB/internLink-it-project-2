<div class="layout-container">
    <header>
        <div class="logo">
            <h1>Career Launch</h1>
            <p>Jouw carrière begint hier</p>
        </div>
        <nav>
            <a href="/login/">Login</a>
            <a href="/register/">Register</a>
            <a href="/">Home</a>
        </nav>
    </header>

    <!-- Hoofdinhoud van de pagina -->
    <main>
        {@render children()} <!-- Dit is waar de inhoud van pagina's (zoals +page.svelte) komt -->
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Career Launch | Alle rechten voorbehouden</p>
    </footer>
</div>

<style>
    .layout-container {
        display: flex;
        flex-direction: column;
        height: 100vh;
        background-size: cover;
    }

    header {
        padding: 1rem;
        background-color: rgba(0, 0, 0, 0.5); /* Transparante achtergrond */
        color: white;
        text-align: center;
    }

    .logo h1 {
        margin: 0;
        font-size: 2.5rem;
        font-weight: bold;
    }

    .logo p {
        margin: 0.5rem 0;
        font-size: 1.2rem;
    }

    nav a {
        margin: 0 1rem;
        text-decoration: none;
        color: white;
        font-weight: bold;
    }

    nav a:hover {
        text-decoration: underline;
    }

    main {
        flex: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
    }

    footer {
        text-align: center;
        padding: 1rem;
        background-color: rgba(0, 0, 0, 0.7);
        color: white;
    }
</style>