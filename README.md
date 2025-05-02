# Ex.07 Restaurant Website
## Date:02.05.2025
## Developed by: Deepika S
Reg No: 212223230039

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>TasteBuds – Fresh • Local • Delicious</title>

    <!-- ===== Basic styling in‑file for convenience ===== -->
    <style>
        :root {
            --primary: #c0392b;              /* tomato red */
            --dark: #222;                    /* near‑black */
            --light: #fafafa;
        }

        /* reset */
        * {margin:0;padding:0;box-sizing:border-box;font-family: 'Segoe UI', sans-serif;}

        body {background: var(--light); color: var(--dark); line-height: 1.6;}

        /* ----- NAVBAR ----- */
        header {
            background: var(--dark);
            color: white;
            position: sticky; top: 0; z-index: 1000;
        }
        nav {display: flex; align-items: center; justify-content: space-between; max-width: 1100px; margin: auto; padding: 1rem;}
        nav a.logo {font-size: 1.4rem; font-weight: 600; color: white; text-decoration: none;}
        ul.nav-links {list-style: none; display: flex; gap: 1.5rem;}
        ul.nav-links a {color: white; text-decoration: none; border-bottom: 2px solid transparent; padding-bottom: 2px;}
        ul.nav-links a:hover {border-color: var(--primary);}

        /* ----- HERO / BANNER ----- */
        .hero {
            background: url("C:\Users\admin\Downloads\bg.jpg") center/cover no-repeat;
            height: 75vh;
            display:flex; align-items:center; justify-content:center;
            text-align: center;
            color: white;
            position: relative;
        }
        .hero::before {content:"";position:absolute;inset:0;background:rgba(0,0,0,0.55);}
        .hero .text {position: relative; z-index: 2;}
        .hero h1 {font-size: clamp(2.5rem, 6vw, 4rem); letter-spacing: .05em;}
        .hero p {margin:.8rem 0 1.5rem;}
        .btn {
            display:inline-block; background: var(--primary); color: white; padding:.7rem 1.6rem;
            border-radius: 4px; text-decoration: none; transition: background .25s;
        }
        .btn:hover {background:#e74c3c;}

        /* ----- SECTIONS ----- */
        section {padding: 4rem 1rem;}
        .container {max-width: 1000px; margin:auto;}

        /* menu grid */
        .menu-grid {display:grid; gap:1.5rem; grid-template-columns: repeat(auto-fit, minmax(250px,1fr));}
        .dish {background:white; border-radius:6px; overflow:hidden; box-shadow:0 2px 8px rgba(0,0,0,.07);}
        .dish img {width:100%; height:170px; object-fit:cover;}
        .dish h3 {padding:.8rem 1rem .3rem;}
        .dish p {padding:0 1rem 1rem; font-size:.9rem; color:#555;}

        /* gallery */
        .gallery {display:grid; gap:10px; grid-template-columns:repeat(auto-fill,minmax(180px,1fr));}
        .gallery img {width:100%; height:150px; object-fit:cover; border-radius:4px;}

        /* contact form */
        form {display:grid; gap:1rem; max-width:500px;}
        input, textarea {padding:.7rem; border:1px solid #ccc; border-radius:4px; font-size:1rem;}
        textarea {resize:vertical; min-height:120px;}

        /* footer */
        footer {background: var(--dark); color:white; text-align:center; padding:1.5rem;}
    </style>
</head>
<body>

    <!-- ===== NAVBAR ===== -->
    <header>
        <nav>
            <a href="#" class="logo">TasteBuds</a>
            <ul class="nav-links">
                <li><a href="#menu">Menu</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- ===== HERO ===== -->
    <section class="hero">
        <div class="text">
            <h1>Welcome to TasteBuds</h1>
            <p>Fresh ingredients, cozy atmosphere, unforgettable flavors.</p>
            <a href="#menu" class="btn">View Menu</a>
        </div>
    </section>

    <!-- ===== MENU SECTION ===== -->
    <section id="menu">
        <div class="container">
            <h2>Our Favourites</h2><br/>
            <div class="menu-grid">
                <article class="dish">
                    <img src="c:\Users\admin\Downloads\pasyta.jpg" alt="Pasta Primavera">
                    <h3>Pasta Primavera</h3>
                    <p>Seasonal vegetables tossed with house‑made fettuccine in a light garlic sauce.</p>
                </article>
                <article class="dish">
                    <img src="c:\Users\admin\Downloads\burger.jpg" alt="Gourmet Burger">
                    <h3>Gourmet Burger</h3>
                    <p>Grass‑fed beef, aged cheddar, caramelised onions &amp; our special sauce.</p>
                </article>
                <article class="dish">
                    <img src="c:\Users\admin\Downloads\salad.jpg" alt="Garden Salad">
                    <h3>Garden Salad</h3>
                    <p>Crisp lettuce, heirloom tomatoes, feta cheese &amp; lemon vinaigrette.</p>
                </article>
            </div>
        </div>
    </section>

    <!-- ===== ABOUT SECTION ===== -->
    <section id="about" style="background:#fff5f2;">
        <div class="container">
            <h2>About Us</h2><br/>
            <p>
                Family‑owned since 1998, TasteBuds is committed to sustainable sourcing and
                the warm hospitality that makes you feel at home. Every dish is prepared from scratch
                using local produce and time‑honoured recipes.
            </p>
        </div>
    </section>

    <!-- ===== GALLERY SECTION ===== -->
    <section id="gallery">
        <div class="container">
            <h2>Gallery</h2><br/>
            <div class="gallery">
                <img src="c:\Users\admin\Downloads\interior.jpg" alt="Restaurant interior" />
                <img src="c:\Users\admin\Downloads\chef.jpg" alt="Chef at work" />
                <img src="c:\Users\admin\Downloads\desert.jpg" alt="Dessert display" />
                <img src="c:\Users\admin\Downloads\od.jpg" alt="Outdoor seating" />
            </div>
        </div>
    </section>

    <!-- ===== CONTACT SECTION ===== -->
    <section id="contact" style="background:#f2f6ff;">
        <div class="container">
            <h2>Contact Us</h2><br/>
            <form>
                <input type="text" placeholder="Name" required />
                <input type="email" placeholder="Email" required />
                <textarea placeholder="Your message…"></textarea>
                <button class="btn" type="submit">Send</button>
            </form>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer>
        © 2025 TasteBuds • 123 Main Street, Hometown • (555) 123‑4567
    </footer>

</body>
</html>

```


## OUTPUT:
![alt text](<Screenshot 2025-05-02 175129.png>)
![alt text](<Screenshot 2025-05-02 175149.png>)
![alt text](<Screenshot 2025-05-02 175208.png>)
![alt text](<Screenshot 2025-05-02 175219.png>)
## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
