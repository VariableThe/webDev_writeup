# Creating a Portfolio Website:
What I'm thinking we can do is create multiple pages and link them to one another use a nav bar located in  the header.<br>
After creating all the files and writing the home page, it looks like:
`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aditya - Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Home</h1>
        <nav>
            <ul>
                <li><a href="about.html">About</a></li>
                <li><a href="portfolio.html">Portfolio</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
        <img src="logo_fin.jpeg" alt="logo" class="logo">
    </header>

    <section id="about">
        <h2>Introduction:</h2>
        <p>Welcome to my portfolio website! My name is Aditya and I'm passionate about coding and games. <br>
        This website serves as a showcase of my work and accomplishments. <br>
        Here, you'll find information about my background, projects I've worked on, and how to get in touch with me.
        Feel free to explore and learn more about what I have to offer!</p>
    </section>
    
    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
`

