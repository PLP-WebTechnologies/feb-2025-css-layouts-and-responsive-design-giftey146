# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive CSS Layout</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="navbar">
    <h1 class="logo">MySite</h1>
    <nav class="nav-links">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Services</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <main class="container">
    <section class="main-content">
      <h2>Welcome</h2>
      <p>This is the main content area.</p>
    </section>
    <aside class="sidebar">
      <h3>Sidebar</h3>
      <p>Some extra info here.</p>
    </aside>
  </main>

  <footer class="footer">
    <p>&copy; 2025 MySite. All rights reserved.</p>
  </footer>
</body>
</html>


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #222;
  padding: 1rem;
  color: white;
}

.nav-links a {
  margin-left: 1rem;
  color: white;
  text-decoration: none;
}

.container {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 1rem;
  padding: 1rem;
}

.main-content, .sidebar {
  background-color: #f4f4f4;
  padding: 1rem;
  border-radius: 8px;
}

.footer {
  text-align: center;
  padding: 1rem;
  background-color: #eee;
  margin-top: 1rem;
}

/* Responsive Design */
@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
  }

  .nav-links {
    display: none;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .container {
    grid-template-columns: 3fr 2fr;
  }
}


