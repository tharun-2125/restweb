# Ex.07 Restaurant Website
## Date:25/12/25

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
~~~
home.html
{% load static %}
<!DOCTYPE html>

<html>

<head>

<title>hot flavs</title>

<link rel="stylesheet" href="{%static 'index.css' %}">

</head>

<body>

<header>

<h1>hot flavs</h1>

</header>

<nav>


<a href="{% url 'home' %}">Home</a>

<a href="{% url 'menu' %}">Menu</a>

<a href="{% url 'admin' %}">Administration</a>


<a href="{% url 'contact' %}">Contact Us</a>

</nav>

<section>

<img src="{% static 'galleryapp/restaurant.jpg'}" alt="Restaurant Banner">


<h2>Welcome to hot flavs</h2>

<p>Authentic flavors, fresh ingredients, and a cozy dining experience.</p>

</section>

<footer>
 <p> 2025 hot flavs</p>
</footer>

</body>

</html>

menu.html
 {% load static %}
 <!DOCTYPE html>

<html>

<head>

<meta charset="UTF-8">

<title>hot flavs - Menu</title>

<link rel="stylesheet" href="{% static 'index.css' %}">

</head>

<body>

<header>

<h1>hot flavs</h1>

</header>

<nav>


<a href="{% url 'home' %}">Home</a>

<a href="{% url 'menu' %}">Menu</a>

<a href="{% url 'admin' %}">Administration</a>


<a href="{% url 'contact' %}">Contact Us</a>

</nav>

<section>

<div class="menu">

  <div class="card">
    <img src="{% static 'galleryapp/grilled_chicken.jpg' %}" alt="Grilled Chicken">
    <p>Grilled Chicken – ₹660</p>
  </div>

  <div class="card">
    <img src="{% static 'galleryapp/veg_pulaw.jpg' %}" alt="Veg Pulaw">
    <p>Veg Pulaw – ₹360</p>
  </div>

  <div class="card">
    <img src="{% static 'galleryapp/chicken_tikka.jpg' %}" alt="Chicken Tikka">
    <p>Chicken Tikka – ₹320</p>
  </div>

  <div class="card">
    <img src="{% static 'galleryapp/chicken_pizza.jpg' %}" alt="Chicken Pizza">
    <p>Chicken Pizza – ₹250</p>
  </div>

  <div class="card">
    <img src="{% static 'galleryapp/panneer_butter.jpg' %}" alt="Paneer Butter Masala">
    <p>Paneer Butter Masala – ₹280</p>
  </div>

</div>

</section>

<footer>


</footer>

</body>

</html>

admin.html
{% load static %}
<!DOCTYPE html>

<html>

<head>

<title>hot flavs - Administration</title>

<link rel="stylesheet" href="{% static 'index.css' %}">

</head>

<body>

<header>

<h1>hot flavs Restaurant</h1>

</header>

<nav>


<a href="{% url 'home' %}">Home</a>

<a href="{% url 'menu' %}">Menu</a>

<a href="{% url 'admin' %}">Administration</a>


<a href="{% url 'contact' %}">Contact Us</a>

</nav>

<section>

<h2>Meet Our Team</h2>

<div class="team-grid">

<div class="card"><img src="{% static 'galleryapp/my_img.jpg' %}"  alt="team member">
<p>Person 1 - Head Chef</p></div>

</div>

</section>
</body>

</html>

contact.html
{% load static %}
<!DOCTYPE html>

<html>

<head>

<meta charset="UTF-8">

<title>hot flavs - Contact Us</title>

<link rel="stylesheet" href="{% static 'index.css' %}">

</head>

<body>

<header>

<h1>hot flavs Restaurant</h1>

</header>

<nav>

<a href="{% url 'home' %}">Home</a>

<a href="{% url 'menu' %}">Menu</a>

<a href="{% url 'admin' %}">Administration</a>

<a href="{% url 'contact' %}">Contact Us</a>

</nav>

<section>

<div class="contact-container">

<h2>Contact Us</h2>

<p><b>Address:</b> No. 83, Anna

Salai, Mount Road, Chennai, Tamil Nadu 600002</p>

<p><b>Phone:</b> +91

9342877348</p>

<p><b>Email:</b> tharunnatarajan2125@gmail.com</p>
<p><b>Opening Hours:</b> Mon-Sun:

10:00 AM - 10:00 PM</p>

</div>

</section>

<footer>

.

</footer>

</body>

</html>

index.css
/* =========================
   GLOBAL RESET & BODY
========================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
}

body {
    background-color: #9b1616;
    color: #333;
}

/* =========================
   HEADER
========================= */
header {
    background-color: #b22222;
    color: white;
    text-align: center;
    padding: 20px;
}

header h1 {
    font-size: 36px;
    letter-spacing: 2px;
}

/* =========================
   NAVBAR
========================= */
nav {
    background-color: #222;
    display: flex;
    justify-content: center;
    gap: 25px;
    padding: 15px 0;
}

nav a {
    color: rgb(163, 129, 129);
    text-decoration: none;
    font-size: 18px;
    padding: 8px 16px;
    border-radius: 5px;
    transition: 0.3s;
}

nav a:hover {
    background-color: #b22222;
}

/* =========================
   SECTION COMMON
========================= */
section {
    padding: 40px 20px;
    text-align: center;
}

/* =========================
   HOME PAGE
========================= */
section img {
    width: 90%;
    max-width: 90px;
    border-radius: 12px;
    margin-bottom: 10px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
}

section h2 {
    font-size: 60px;
    color: #b22222;
    margin-bottom: 20px;
}

section p {
    font-size: 50px;
    max-width: 650px;
    margin: auto;
    line-height: 1.6;
}

/* =========================
   MENU PAGE
========================= */
.menu {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 25px;
    max-width: 1100px;
    margin: auto;
}

.card {
    background-color: rgb(15, 14, 14);
    border-radius: 12px;
    overflow: hidden;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0,0,0,0.15);
    transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 18px rgba(0,0,0,0.25);
}

.card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.card p {
    font-size: 120px;
    font-weight: bold;
    padding: 15px;
    color: #b22222;
}

/* =========================
   CONTACT PAGE
========================= */
.contact-container {
    max-width: 700px;
    margin: auto;
    background-color: white;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.contact-container h2 {
    font-size: 30px;
    color: #9a4b4b;
    margin-bottom: 20px;
}

.contact-container p {
    font-size: 18px;
    margin: 12px 0;
    line-height: 1.6;
}

/* =========================
   ADMIN PAGE
========================= */
.team-grid {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
}

.team-grid .card {
    width: 260px;
}

.team-grid .card img {
    height: 260px;
}

/* =========================
   FOOTER
========================= */
footer {
    background-color: #222;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 40px;
}

~~~


## OUTPUT:
<img width="1920" height="1080" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/5521c0e3-2636-4676-9258-287fbe7ad18b" />
<img width="1920" height="1080" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/21f9e95b-d487-4c73-add6-6172ded32de3" />
<img width="1920" height="1080" alt="Screenshot (69)" src="https://github.com/user-attachments/assets/fda8086e-0c27-4fc0-a9a3-85c42f556b18" />
<img width="1920" height="1080" alt="Screenshot (70)" src="https://github.com/user-attachments/assets/894e315e-68a1-4dcb-bcd6-60a7a06335a6" />






## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
