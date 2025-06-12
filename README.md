<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout</title>
  <style>
    /* Reset & base styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }

    /* Navigation Bar (Flexbox) */
    nav {
      background: #333;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
    }

    nav ul {
      display: flex;
      list-style: none;
    }

    nav ul li {
      margin-left: 1rem;
    }

    nav a {
      color: white;
      text-decoration: none;
    }

    /* Grid Layout */
    .container {
      display: grid;
      grid-template-areas:
        "main"
        "sidebar";
      gap: 1rem;
      padding: 1rem;
    }

    .main {
      grid-area: main;
      background: #f4f4f4;
      padding: 1rem;
    }

    .sidebar {
      grid-area: sidebar;
      background: #ddd;
      padding: 1rem;
    }

    /* Responsive Design with Media Queries */
    @media (min-width: 600px) {
      .container {
        grid-template-areas: "main sidebar";
        grid-template-columns: 2fr 1fr;
      }
    }

    @media (min-width: 900px) {
      nav {
        padding: 1.5rem 3rem;
      }

      .container {
        grid-template-columns: 3fr 1fr;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <nav>
    <div class="logo">MySite</div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Grid Layout -->
  <div class="container">
    <div class="main">
      <h1>Welcome</h1>
      <p>This is the main content area.</p>
    </div>
    <div class="sidebar">
      <h2>Sidebar</h2>
      
    </div>
  </div>

</body>
</html>

