# Creating a Portfolio Website:
What I'm thinking we can do is create multiple pages and link them to one another use a nav bar located in  the header.<br>
After creating all the files and writing the home page, it looks like:
```
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
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>Home</h1>
        <nav>
            <ul>
                <li><a href="about.html" class="button2">About</a></li>
                <li><a href="portfolio.html" class="button2">Portfolio</a></li>
                <li><a href="contact.html" class="button2">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="about">
        <h2>Introduction:</h2>
        <p class="boxed">Welcome to my portfolio website! My name is Aditya and I'm passionate about coding and games. <br>
        This website serves as a showcase of my work and accomplishments. <br>
        Here, you'll find information about my background, projects I've worked on, and how to get in touch with me.
        Feel free to explore and learn more about what I have to offer!</p>
    </section>
    
    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
What I have done now is created about, contact and portfolio pages aswell, following the same pattern an using a button I found from [here](uiverse.io).
The css file looks like this:
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #3c3c3c;
    color: #fff;
    padding-left: 20px;
}

header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #21201d;
    color: #fff;
    padding: 20px;
    margin-left: -20px;
}

header h1 {
    margin: 0;
    font-size: 2em;
}

header img.logo {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
}

nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

nav ul li {
    display: inline;
    margin-right: 20px;
}

nav ul li a {
    text-decoration: none;
}

.button2 {
    display: inline-block;
    transition: all 0.2s ease-in;
    position: relative;
    overflow: hidden;
    z-index: 1;
    color: #ffffff;
    padding: 0.5em 1.2em;
    cursor: pointer;
    font-size: 18px;
    border-radius: 0.5em;
    background: #21201d;
    border: 1px solid #21201d;
    box-shadow: 6px 6px 12px #1a1a1a, -6px -6px 12px #2b2b2b;
    margin-left: 5px;
    width: 25%;
}



.button2:active {
    color: #666;
    box-shadow: inset 4px 4px 12px #1a1a1a, inset -4px -4px 12px #2b2b2b;
}

.button2:before {
    content: "";
    position: absolute;
    left: 50%;
    transform: translateX(-50%) scaleY(1) scaleX(1.25);
    top: 100%;
    width: 140%;
    height: 180%;
    background-color: rgba(0, 0, 0, 0.05);
    border-radius: 50%;
    display: block;
    transition: all 0.5s 0.1s cubic-bezier(0.55, 0, 0.1, 1);
    z-index: -1;
}

.button2:after {
    content: "";
    position: absolute;
    left: 55%;
    transform: translateX(-50%) scaleY(1) scaleX(1.45);
    top: 180%;
    width: 160%;
    height: 190%;
    background-color: #009087;
    border-radius: 50%;
    display: block;
    transition: all 0.5s 0.1s cubic-bezier(0.55, 0, 0.1, 1);
    z-index: -1;
}

.button2:hover {
    color: #ffffff;
    border: 1px solid #ff67e3;
}

.button2:hover:before {
    top: -35%;
    background-color: #ff67e3;
    transform: translateX(-50%) scaleY(1.3) scaleX(0.8);
}

.button2:hover:after {
    top: -45%;
    background: linear-gradient(to left, #ff67e3, #e41229);
    transform: translateX(-50%) scaleY(1.3) scaleX(0.8);
}

section {
    padding: 20px;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
    margin-left: -20px;
}

.boxed {
    background-color: #002951;
    padding: 20px;
    border-radius: 10px; 
    margin: 20px 0;
}
```
So, with that out of the way, This is how the about, contact and portfolio pages look at the moment:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me - Aditya</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>About</h1>
        <nav>
            <ul>
                <li><a href="index.html" class="button2">Home</a></li>
                <li><a href="portfolio.html" class="button2">Portfolio</a></li>
                <li><a href="contact.html" class="button2">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="about">
        <h2>About Me</h2>
        <p class="boxed">Currently I'm a second year student in the Manipal Institue of technology, I'm undertaking the B.Tech course of Computer Science and Financial technology. I'm usually quite curious and love brain teasers. I also indulge quite a lot in playing video games and reading novels. I'm not really an extrovert, but I like hanging out with my friends and talking about differen topics.</p>
    </section>

    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact - Aditya</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>Contact</h1>
        <nav>
            <ul>
                <li><a href="index.html" class="button2">Home</a></li>
                <li><a href="about.html" class="button2">About</a></li>
                <li><a href="portfolio.html" class="button2">Portfolio</a></li>
            </ul>
        </nav>
    </header>

    <section id="contact">
        <h2>Contact Me</h2>
        <p class="boxed">Email: slayermk57@gmail.com<br>
           Phone: 7032579820</p>
    </section>

    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - Aditya</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>Portfolio</h1>
        <nav>
            <ul>
                <li><a href="index.html" class="button2">Home</a></li>
                <li><a href="about.html" class="button2">About</a></li>
                <li><a href="contact.html" class="button2">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="portfolio">
        <h2>Portfolio</h2>
         <p  class="boxed">Hello</p>
    </section>

    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
With all the preliminary coding now done, I think it's time to add the actual information.<br>
I've done that, but I feel it might not be enough, so I searched [here](uiverse.io) for forms that I use in the contact me page, and found one.<br>
Now that I have added it in contact.html like this:
```
<div class="form-container">
      <form class="form">
        <div class="form-group">
          <label for="email">Your Email</label>
          <input type="text" id="email" name="email" required="">
        </div>
        <div class="form-group">
          <label for="textarea">What can I do for you</label>
          <textarea name="textarea" id="textarea" rows="10" cols="50" required="">          </textarea>
        </div>
        <button class="form-submit-btn" type="submit">Submit</button>
      </form>
    </div>
```
The css file was updated like so:
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #3c3c3c;
    color: #fff;
    padding-left: 20px;
}

header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #21201d;
    color: #fff;
    padding: 20px;
    margin-left: -20px;
}

header h1 {
    margin: 0;
    font-size: 2em;
}

header img.logo {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
}

nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

nav ul li {
    display: inline;
    margin-right: 20px;
}

nav ul li a {
    text-decoration: none;
}

.button2 {
    display: inline-block;
    transition: all 0.2s ease-in;
    position: relative;
    overflow: hidden;
    z-index: 1;
    color: #ffffff;
    padding: 0.5em 1.2em;
    cursor: pointer;
    font-size: 18px;
    border-radius: 0.5em;
    background: #21201d;
    border: 1px solid #21201d;
    box-shadow: 6px 6px 12px #1a1a1a, -6px -6px 12px #2b2b2b;
    margin-left: 5px;
    width: 25%;
}



.button2:active {
    color: #666;
    box-shadow: inset 4px 4px 12px #1a1a1a, inset -4px -4px 12px #2b2b2b;
}

.button2:before {
    content: "";
    position: absolute;
    left: 50%;
    transform: translateX(-50%) scaleY(1) scaleX(1.25);
    top: 100%;
    width: 140%;
    height: 180%;
    background-color: rgba(0, 0, 0, 0.05);
    border-radius: 50%;
    display: block;
    transition: all 0.5s 0.1s cubic-bezier(0.55, 0, 0.1, 1);
    z-index: -1;
}

.button2:after {
    content: "";
    position: absolute;
    left: 55%;
    transform: translateX(-50%) scaleY(1) scaleX(1.45);
    top: 180%;
    width: 160%;
    height: 190%;
    background-color: #009087;
    border-radius: 50%;
    display: block;
    transition: all 0.5s 0.1s cubic-bezier(0.55, 0, 0.1, 1);
    z-index: -1;
}

.button2:hover {
    color: #ffffff;
    border: 1px solid #ff67e3;
}

.button2:hover:before {
    top: -35%;
    background-color: #ff67e3;
    transform: translateX(-50%) scaleY(1.3) scaleX(0.8);
}

.button2:hover:after {
    top: -45%;
    background: linear-gradient(to left, #ff67e3, #e41229);
    transform: translateX(-50%) scaleY(1.3) scaleX(0.8);
}

section {
    padding: 20px;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
    margin-left: -20px;
}

.boxed {
    background-color: #002951;
    padding: 20px;
    border-radius: 10px; 
    margin: 20px 0;
}
.form-container {
  width: 400px;
  background: linear-gradient(#212121, #212121) padding-box,
              linear-gradient(145deg, transparent 35%,#e81cff, #40c9ff) border-box;
  border: 2px solid transparent;
  padding: 32px 24px;
  font-size: 14px;
  font-family: Arial, sans-serif;
  color: white;
  display: flex;
  flex-direction: column;
  gap: 20px;
  box-sizing: border-box;
  border-radius: 16px;
  margin: 0 auto; 
  margin-bottom: 80px;
}


.form-container button:active {
  scale: 0.95;
}

.form-container .form {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.form-container .form-group {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.form-container .form-group label {
  display: block;
  margin-bottom: 5px;
  color: #717171;
  font-weight: 600;
  font-size: 12px;
}

.form-container .form-group input {
  width: 100%;
  padding: 12px 16px;
  border-radius: 8px;
  color: #fff;
  font-family: inherit;
  background-color: transparent;
  border: 1px solid #414141;
}

.form-container .form-group textarea {
  width: 100%;
  padding: 12px 16px;
  border-radius: 8px;
  resize: none;
  color: #fff;
  height: 96px;
  border: 1px solid #414141;
  background-color: transparent;
  font-family: inherit;
}

.form-container .form-group input::placeholder {
  opacity: 0.5;
}

.form-container .form-group input:focus {
  outline: none;
  border-color: #e81cff;
}

.form-container .form-group textarea:focus {
  outline: none;
  border-color: #e81cff;
}

.form-container .form-submit-btn {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  align-self: flex-start;
  font-family: inherit;
  color: #717171;
  font-weight: 600;
  width: 40%;
  background: #313131;
  border: 1px solid #414141;
  padding: 12px 16px;
  font-size: inherit;
  gap: 8px;
  margin-top: 8px;
  cursor: pointer;
  border-radius: 6px;
}

.form-container .form-submit-btn:hover {
  background-color: #fff;
  border-color: #fff;
}
```
It's done and the form is working properly.<br>
I'm done for now, if I add something after that, I'll update it here.<br>
I've updated the button width to 27%, so that it looks better.<br>
Ok, I made a few update, removed the buttons and added a drop down menu to replace it in order to increase the responsiveness.<br>

## The new code:
### index.html:
```
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
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>Home</h1>
        <div class="menu">
            <div class="item">
                <a href="#" class="link">
                    <span> Navigate </span>
                    <svg viewBox="0 0 360 360" xml:space="preserve">
                        <g id="SVGRepo_iconCarrier">
                            <path
                                id="XMLID_225_"
                                d="M325.607,79.393c-5.857-5.857-15.355-5.858-21.213,0.001l-139.39,139.393L25.607,79.393 c-5.857-5.857-15.355-5.858-21.213,0.001c-5.858,5.858-5.858,15.355,0,21.213l150.004,150c2.813,2.813,6.628,4.393,10.606,4.393 s7.794-1.581,10.606-4.394l149.996-150C331.465,94.749,331.465,85.251,325.607,79.393z"
                            ></path>
                        </g>
                    </svg>
                </a>
                <div class="submenu">
                    <div class="submenu-item">
                        <a href="about.html" class="submenu-link"> About </a>
                    </div>
                    <div class="submenu-item">
                        <a href="portfolio.html" class="submenu-link"> Portfolio </a>
                    </div>
                    <div class="submenu-item">
                        <a href="contact.html" class="submenu-link"> Contact </a>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <section id="about">
        <h2>Introduction:</h2>
        <p class="boxed">Welcome to my portfolio website! My name is Aditya and I'm passionate about coding and games. <br>
        This website serves as a showcase of my work and accomplishments. <br>
        Here, you'll find information about my background, projects I've worked on, and how to get in touch with me.
        Feel free to explore and learn more about what I have to offer!</p>
    </section>
    
    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
### about.html:
```
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
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>About</h1>
        <div class="menu">
            <div class="item">
                <a href="#" class="link">
                    <span> Navigate </span>
                    <svg viewBox="0 0 360 360" xml:space="preserve">
                        <g id="SVGRepo_iconCarrier">
                            <path
                                id="XMLID_225_"
                                d="M325.607,79.393c-5.857-5.857-15.355-5.858-21.213,0.001l-139.39,139.393L25.607,79.393 c-5.857-5.857-15.355-5.858-21.213,0.001c-5.858,5.858-5.858,15.355,0,21.213l150.004,150c2.813,2.813,6.628,4.393,10.606,4.393 s7.794-1.581,10.606-4.394l149.996-150C331.465,94.749,331.465,85.251,325.607,79.393z"
                            ></path>
                        </g>
                    </svg>
                </a>
                <div class="submenu">
                    <div class="submenu-item">
                        <a href="index.html" class="submenu-link"> Home
                        </a>
                    </div>
                    <div class="submenu-item">
                        <a href="portfolio.html" class="submenu-link"> Portfolio </a>
                    </div>
                    <div class="submenu-item">
                        <a href="contact.html" class="submenu-link"> Contact </a>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <section id="about">
        <h2>About Me</h2>
        <p class="boxed">Currently I'm a second year student in the Manipal Institue of technology, I'm undertaking the B.Tech course of Computer Science and Financial technology. I'm usually quite curious and love brain teasers. I also indulge quite a lot in playing video games and reading novels. I'm not really an extrovert, but I like hanging out with my friends and talking about differen topics.</p>
    </section>

    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
### portfolio.html:
```
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
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>Portfolio</h1>
        <div class="menu">
            <div class="item">
                <a href="#" class="link">
                    <span> Navigate </span>
                    <svg viewBox="0 0 360 360" xml:space="preserve">
                        <g id="SVGRepo_iconCarrier">
                            <path
                                id="XMLID_225_"
                                d="M325.607,79.393c-5.857-5.857-15.355-5.858-21.213,0.001l-139.39,139.393L25.607,79.393 c-5.857-5.857-15.355-5.858-21.213,0.001c-5.858,5.858-5.858,15.355,0,21.213l150.004,150c2.813,2.813,6.628,4.393,10.606,4.393 s7.794-1.581,10.606-4.394l149.996-150C331.465,94.749,331.465,85.251,325.607,79.393z"
                            ></path>
                        </g>
                    </svg>
                </a>
                <div class="submenu">
                    <div class="submenu-item">
                        <a href="about.html" class="submenu-link"> About </a>
                    </div>
                    <div class="submenu-item">
                        <a href="index.html" class="submenu-link"> Home </a>
                    </div>
                    <div class="submenu-item">
                        <a href="contact.html" class="submenu-link"> Contact </a>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <section id="portfolio">
        <h2>Portfolio</h2>
         <p  class="boxed">I have a decent amount of skills, some software and some social skills some achievements I have under my belt are:
        <br>
             I have an understanding of a few coding languages, like Python, C and C#<br>
             I have made an endless runner from scratch before.<br>
             I have a basic understanding and user experience for blender.<br>
             I also have years of experience using productivity apps, such as word, powerpoint and excel.<br>
             I also have dabbled in animation and arts and crafts, not origamni, but more side stream content like wood working.<br>
             Although not popular, I also have a youtube channel and utilize plenty of my editing, public speaking and other various skills there.<br>
             I have had to deal with all types of people in my life and have naturally come to be able handle most of them. I believe I am more active and participating than the average person.<br>
             I am also quite humourous and get along well with people.
        </p>
    </section>

    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
</body>
</html>
```
### contact.html:
```
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
        <img src="logo_fin.jpeg" alt="logo" class="logo">
        <h1>Contact</h1>
        <div class="menu">
            <div class="item">
                <a href="#" class="link">
                    <span> Navigate </span>
                    <svg viewBox="0 0 360 360" xml:space="preserve">
                        <g id="SVGRepo_iconCarrier">
                            <path
                                id="XMLID_225_"
                                d="M325.607,79.393c-5.857-5.857-15.355-5.858-21.213,0.001l-139.39,139.393L25.607,79.393 c-5.857-5.857-15.355-5.858-21.213,0.001c-5.858,5.858-5.858,15.355,0,21.213l150.004,150c2.813,2.813,6.628,4.393,10.606,4.393 s7.794-1.581,10.606-4.394l149.996-150C331.465,94.749,331.465,85.251,325.607,79.393z"
                            ></path>
                        </g>
                    </svg>
                </a>
                <div class="submenu">
                    <div class="submenu-item">
                        <a href="about.html" class="submenu-link"> About </a>
                    </div>
                    <div class="submenu-item">
                        <a href="portfolio.html" class="submenu-link"> Portfolio </a>
                    </div>
                    <div class="submenu-item">
                        <a href="index.html" class="submenu-link"> Home </a>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <section id="contact">
        <h2>Contact Me</h2>
        <p class="boxed">Email: slayermk57@gmail.com<br>
           Phone: 7032579820</p>
    </section>

    <footer>
        <p>&copy; 2024 The Variable</p>
    </footer>
    <div class="form-container">
      <form class="form">
        <div class="form-group">
          <label for="email">Your Email</label>
          <input type="text" id="email" name="email" required="">
        </div>
        <div class="form-group">
          <label for="textarea">What can I do for you</label>
          <textarea name="textarea" id="textarea" rows="10" cols="50" required="">          </textarea>
        </div>
        <button class="form-submit-btn" type="submit">Submit</button>
      </form>
    </div>
</body>
</html>
```
### style.css
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #3c3c3c;
    color: #fff;
    padding-left: 20px;
}

header {
    display: flex;
    align-items: center;
    background-color: #21201d;
    color: #fff;
    padding: 20px;
    margin-left: -20px;
}

header h1 {
    margin: 0 0 0 10px;
    font-size: 2em;
}

header img.logo {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
}

.menu {
    font-size: 12px;
    line-height: 1.6;
    color: #ffffff;
    width: fit-content;
    display: flex;
    list-style: none;
    margin-left: auto;
}

.menu a {
    text-decoration: none;
    color: inherit;
    font-family: inherit;
    font-size: inherit;
    line-height: inherit;
}

.menu .link {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    padding: 12px 36px;
    border-radius: 16px;
    overflow: hidden;
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
    color: #ffffff;
}

.menu .link::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #0a3cff;
    z-index: -1;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.menu .link svg {
    width: 14px;
    height: 14px;
    fill: #ffffff;  /* Ensure SVG color is white */
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.menu .item {
    position: relative;
}

.menu .item .submenu {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    top: 100%;
    border-radius: 0 0 16px 16px;
    left: 0;
    width: 100%;
    overflow: hidden;
    border: 1px solid #cccccc;
    opacity: 0;
    visibility: hidden;
    transform: translateY(-12px);
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
    z-index: 1;
    pointer-events: none;
    list-style: none;
}

.menu .item:hover .submenu {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
    pointer-events: auto;
    border-top: transparent;
    border-color: #0a3cff;
}

.menu .item:hover .link {
    color: #ffffff;
    border-radius: 16px 16px 0 0;
}

.menu .item:hover .link::after {
    transform: scaleX(1);
    transform-origin: right;
}

.menu .item:hover .link svg {
    fill: #ffffff;
    transform: rotate(-180deg);
}

.submenu .submenu-item {
    width: 100%;
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.submenu .submenu-link {
    display: block;
    padding: 12px 24px;
    width: 100%;
    position: relative;
    text-align: center;
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
    color: #ffffff;  
}

.submenu .submenu-item:last-child .submenu-link {
    border-bottom: none;
}

.submenu .submenu-link::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    transform: scaleX(0);
    width: 100%;
    height: 100%;
    background-color: #0a3cff;
    z-index: -1;
    transform-origin: left;
    transition: transform 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.submenu .submenu-link:hover:before {
    transform: scaleX(1);
    transform-origin: right;
}

.submenu .submenu-link:hover {
    color: #ffffff;
}

section {
    padding: 20px;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
    margin-left: -20px;
}

.boxed {
    background-color: #002951;
    padding: 20px;
    border-radius: 10px; 
    margin: 20px 0;
}

.form-container {
    width: 390px;
    background: linear-gradient(#212121, #212121) padding-box,
                linear-gradient(145deg, transparent 35%,#e81cff, #40c9ff) border-box;
    border: 2px solid transparent;
    padding: 32px 24px;
    font-size: 14px;
    font-family: Arial, sans-serif;
    color: white;
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    border-radius: 16px;
    margin: 0 auto; 
    margin-bottom: 80px;
}

.form-container .form {
    display: flex;
    flex-direction: column;
}

.form-container .form-group {
    display: flex;
    flex-direction: column;
}

.form-container .form-group label {
    display: block;
    margin-bottom: 5px;
    color: #717171;
    font-weight: 600;
    font-size: 12px;
}

.form-container .form-group input {
    width: 100%;
    padding: 12px 16px;
    border-radius: 8px;
    color: #fff;
    font-family: inherit;
    background-color: transparent;
    border: 1px solid #414141;
}

.form-container .form-group textarea {
    width: 100%;
    padding: 12px 16px;
    border-radius: 8px;
    resize: none;
    color: #fff;
    height: 96px;
    border: 1px solid #414141;
    background-color: transparent;
    font-family: inherit;
}

.form-container .form-group input::placeholder {
    opacity: 0.5;
}

.form-container .form-group input:focus {
    outline: none;
    border-color: #e81cff;
}

.form-container .form-group textarea:focus {
    outline: none;
    border-color: #e81cff;
}

.form-container .form-submit-btn {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    align-self: flex-start;
    font-family: inherit;
    color: #717171;
    font-weight: 600;
    width: 40%;
    background: #313131;
    border: 1px solid #414141;
    padding: 12px 16px;
    font-size: inherit;
    margin-top: 8px;
    cursor: pointer;
    border-radius: 6px;
}

.form-container .form-submit-btn:hover {
    background-color: #fff;
    border-color: #fff;
}
```
And that's the code done.<br>


Ok, new updates to font style and size:
```
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Montserrat', sans-serif;
    line-height: 1.6;
    background-color: #3c3c3c;
    color: #fff;
    padding-left: 20px;
}

header {
    display: flex;
    align-items: center;
    background-color: #21201d;
    color: #fff;
    padding: 20px;
    margin-left: -20px;
}

header h1 {
    margin: 0 0 0 10px;
    font-size: 3em;
    font-family: 'Montserrat', sans-serif;
}

header img.logo {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
}

.menu {
    font-size: 16px;
    line-height: 1.6;
    color: #ffffff;
    width: fit-content;
    display: flex;
    list-style: none;
    margin-left: auto;
}

.menu a {
    text-decoration: none;
    color: inherit;
    font-family: inherit;
    font-size: inherit;
    line-height: inherit;
}

.menu .link {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    padding: 12px 36px;
    border-radius: 16px;
    overflow: hidden;
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
    color: #ffffff;
    font-family: 'Montserrat', sans-serif;
}

.menu .link::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #ff67e0;
    z-index: -1;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.menu .link svg {
    width: 14px;
    height: 14px;
    fill: #ffffff; 
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.menu .item {
    position: relative;
}

.menu .item .submenu {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    top: 100%;
    border-radius: 0 0 16px 16px;
    left: 0;
    width: 100%;
    overflow: hidden;
    border: 1px solid #cccccc;
    opacity: 0;
    visibility: hidden;
    transform: translateY(-12px);
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
    z-index: 1;
    pointer-events: none;
    list-style: none;
}

.menu .item:hover .submenu {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
    pointer-events: auto;
    border-top: transparent;
    border-color: #ff67e0;
}

.menu .item:hover .link {
    color: #ffffff;
    border-radius: 16px 16px 0 0;
}

.menu .item:hover .link::after {
    transform: scaleX(1);
    transform-origin: right;
}

.menu .item:hover .link svg {
    fill: #ffffff;
    transform: rotate(-180deg);
}

.submenu .submenu-item {
    width: 100%;
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.submenu .submenu-link {
    display: block;
    padding: 12px 24px;
    width: 100%;
    position: relative;
    text-align: center;
    transition: all 0.48s cubic-bezier(0.23, 1, 0.32, 1);
    color: #ffffff;  
    font-family: 'Montserrat', sans-serif;
}

.submenu .submenu-item:last-child .submenu-link {
    border-bottom: none;
}

.submenu .submenu-link::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    transform: scaleX(0);
    width: 100%;
    height: 100%;
    background-color: #ff67e0;
    z-index: -1;
    transform-origin: left;
    transition: transform 0.48s cubic-bezier(0.23, 1, 0.32, 1);
}

.submenu .submenu-link:hover:before {
    transform: scaleX(1);
    transform-origin: right;
}

.submenu .submenu-link:hover {
    color: #ffffff;
}

section {
    padding: 20px;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
    margin-left: -20px;
}

.boxed {
    background-color: #002951;
    padding: 20px;
    border-radius: 10px; 
    margin: 20px 0;
}

.form-container {
    width: 390px;
    background: linear-gradient(#212121, #212121) padding-box,
                linear-gradient(145deg, transparent 35%,#e81cff, #40c9ff) border-box;
    border: 2px solid transparent;
    padding: 32px 24px;
    font-size: 14px;
    font-family: 'Montserrat', sans-serif;
    color: white;
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    border-radius: 16px;
    margin: 0 auto; 
    margin-bottom: 80px;
}

.form-container .form {
    display: flex;
    flex-direction: column;
}

.form-container .form-group {
    display: flex;
    flex-direction: column;
}

.form-container .form-group label {
    display: block;
    margin-bottom: 5px;
    color: #717171;
    font-weight: 600;
    font-size: 12px;
    font-family: 'Montserrat', sans-serif;
}

.form-container .form-group input {
    width: 100%;
    padding: 12px 16px;
    border-radius: 8px;
    color: #fff;
    font-family: 'Montserrat', sans-serif;
    background-color: transparent;
    border: 1px solid #414141;
}

.form-container .form-group textarea {
    width: 100%;
    padding: 12px 16px;
    border-radius: 8px;
    resize: none;
    color: #fff;
    height: 96px;
    border: 1px solid #414141;
    background-color: transparent;
    font-family: 'Montserrat', sans-serif;
}

.form-container .form-group input::placeholder {
    opacity: 0.5;
}

.form-container .form-group input:focus {
    outline: none;
    border-color: #e81cff;
}

.form-container .form-group textarea:focus {
    outline: none;
    border-color: #e81cff;
}

.form-container .form-submit-btn {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    align-self: flex-start;
    font-family: 'Montserrat', sans-serif;
    color: #717171;
    font-weight: 600;
    width: 40%;
    background: #313131;
    border: 1px solid #414141;
    padding: 12px 16px;
    font-size: inherit;
    margin-top: 8px;
    cursor: pointer;
    border-radius: 6px;
}

.form-container .form-submit-btn:hover {
    background-color: #fff;
    border-color: #fff;
}
```



