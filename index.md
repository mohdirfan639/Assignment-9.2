Log in
You said:

name=Assignment-9.1.md Assignment 9.1 — Convert a Desktop Page into a Mobile-First Layout[cite: 41] What to build: Make an existing desktop-only webpage responsive[cite: 41]. Steps:

Open the dashboard or photo gallery project from Week 8[cite: 41].
Verify the viewport meta tag in the HTML <head>[cite: 41].
Write CSS for mobile screens first[cite: 41].
Improve tablet and desktop layouts using media queries[cite: 41].
Add at least 2 breakpoints[cite: 41].
Test on different screen sizes using Chrome DevTools' Device Mode[cite: 41].
Fix horizontal overflow and overlapping elements[cite: 41]. Submission: Updated HTML/CSS files and screenshots for mobile, tablet, and desktop[cite: 41]. assignment solve it

ChatGPT said:
Here is a complete solution for Assignment 9.1 — Convert a Desktop Page into a Mobile-First Layout. You can use this as your Week 8 photo gallery project and submit the updated HTML, CSS, and screenshots.

1. Project structure
Create a folder named Assignment-9.1 with these files:


text
Assignment-9.1/
├── index.html
├── style.css
└── screenshots/
    ├── mobile.png
    ├── tablet.png
    └── desktop.png
2. HTML file — index.html
The page includes the required viewport meta tag, a navigation bar, and a responsive photo gallery.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="A responsive photo gallery built with mobile-first CSS.">
    <title>Assignment 9.1 - Photo Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <div class="container navbar">
            <h1 class="logo">PhotoGallery</h1>
            <nav aria-label="Main navigation">
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                    <li><a href="#about">About</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main id="home">
        <section class="hero container">
            <h2>Explore the World</h2>
            <p>
                Discover beautiful places and capture unforgettable
                moments through photography.
            </p>
        </section>

        <section class="gallery-section container" id="gallery">
            <h2>Our Photo Gallery</h2>

            <div class="gallery">
                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=900&q=80"
                        alt="Beautiful mountain landscape">
                    <div class="photo-info">
                        <h3>Mountain View</h3>
                        <p>Nature at its finest.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=900&q=80"
                        alt="Blue ocean and sandy beach">
                    <div class="photo-info">
                        <h3>Sunny Beach</h3>
                        <p>Relax beside the ocean.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1519608487953-e999c86e7455?auto=format&fit=crop&w=900&q=80"
                        alt="Night sky filled with stars">
                    <div class="photo-info">
                        <h3>Starry Night</h3>
                        <p>Beauty under the stars.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=900&q=80"
                        alt="Lake surrounded by green mountains">
                    <div class="photo-info">
                        <h3>Peaceful Lake</h3>
                        <p>A quiet escape into nature.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=900&q=80"
                        alt="Sunlight passing through a forest">
                    <div class="photo-info">
                        <h3>Green Forest</h3>
                        <p>Explore the beauty of trees.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=900&q=80"
                        alt="Tall mountains beneath the sky">
                    <div class="photo-info">
                        <h3>Rocky Peaks</h3>
                        <p>Adventure awaits you.</p>
                    </div>
                </article>
            </div>
        </section>

        <section class="about container" id="about">
            <h2>About Our Gallery</h2>
            <p>
                This photo gallery demonstrates a mobile-first responsive
                layout using CSS Grid, Flexbox, and media queries.
                It adapts to mobile phones, tablets, and desktop screens.
            </p>
        </section>
    </main>

    <footer class="footer">
        <p>&copy; 2026 PhotoGallery | Assignment 9.1</p>
    </footer>

</body>
</html>
3. CSS file — style.css
This stylesheet follows the mobile-first approach: the default styles are for small screens, and two media-query breakpoints improve the tablet and desktop layouts.


css

/* Assignment 9.1: Mobile-First Responsive Layout */

/* 1. Common styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
    color: #263238;
    background-color: #f4f7fb;
}

img {
    display: block;
    width: 100%;
    max-width: 100%;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 16px;
}

/* 2. Header and navigation */
.header {
    background-color: #17324d;
    color: white;
}

.navbar {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    padding-top: 16px;
    padding-bottom: 16px;
}

.logo {
    font-size: 25px;
    line-height: 1.3;
}

.nav-links {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 18px;
    list-style: none;
}

.nav-links a {
    color: white;
    text-decoration: none;
    font-size: 15px;
}

.nav-links a:hover {
    color: #80deea;
}

/* 3. Hero section */
.hero {
    padding-top: 40px;
    padding-bottom: 32px;
    text-align: center;
}

.hero h2 {
    font-size: 30px;
    color: #17324d;
    margin-bottom: 12px;
}

.hero p {
    max-width: 600px;
    margin: 0 auto;
    color: #546575;
}

/* 4. Gallery: one column on mobile */
.gallery-section {
    padding-top: 20px;
    padding-bottom: 40px;
}

.gallery-section > h2,
.about h2 {
    text-align: center;
    font-size: 25px;
    margin-bottom: 24px;
    color: #17324d;
}

.gallery {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 20px;
}

.photo-card {
    min-width: 0;
    overflow: hidden;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.photo-card img {
    width: 100%;
    height: 220px;
    object-fit: cover;
}

.photo-info {
    padding: 16px;
}

.photo-info h3 {
    font-size: 19px;
    margin-bottom: 5px;
    color: #17324d;
}

.photo-info p {
    color: #64748b;
    font-size: 14px;
}

/* 5. About section */
.about {
    padding-top: 20px;
    padding-bottom: 40px;
    text-align: center;
}

.about p {
    max-width: 750px;
    margin: 0 auto;
    color: #546575;
}

/* 6. Footer */
.footer {
    padding: 20px 16px;
    background-color: #17324d;
    color: white;
    text-align: center;
}

/* BREAKPOINT 1: Tablets (600px and above) */
@media screen and (min-width: 600px) {
    .container {
        padding-left: 24px;
        padding-right: 24px;
    }

    .navbar {
        flex-direction: row;
        justify-content: space-between;
    }

    .hero {
        padding-top: 55px;
        padding-bottom: 45px;
    }

    .hero h2 {
        font-size: 38px;
    }

    .gallery {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 24px;
    }

    .photo-card img {
        height: 230px;
    }
}

/* BREAKPOINT 2: Desktops (1024px and above) */
@media screen and (min-width: 1024px) {
    .container {
        padding-left: 32px;
        padding-right: 32px;
    }

    .logo {
        font-size: 29px;
    }

    .nav-links {
        gap: 28px;
    }

    .hero {
        padding-top: 70px;
        padding-bottom: 60px;
    }

    .hero h2 {
        font-size: 46px;
    }

    .gallery {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 28px;
    }

    .photo-card img {
        height: 250px;
        transition: transform 0.3s ease;
    }

    .photo-card:hover img {
        transform: scale(1.04);
    }
}
4. Responsive design breakpoints
Stephen Butler — Brighter Side
Mobile — below 600px

1 column
Navigation items wrap if needed.

Photos appear one below another.

Content fits small screens.

Abi Bacon | UK Squarespace Developer
Tablet — 600px to 1023px

2 columns
Navigation switches to a horizontal layout.

Gallery displays two photos per row.

Spacing increases.

Picfair Themes in-depth - Natural Theme  | Focus
Desktop — 1024px and above

3 columns
Gallery displays three photos per row.

Larger headings and spacing improve readability.

Image hover effects are enabled.

5. How to run and test the assignment
Save index.html and style.css in the same folder.

Open index.html in Google Chrome.

Press F12 to open Chrome DevTools.

Click the Toggle device toolbar icon or press Ctrl + Shift + M.

Test the following screen widths:

Device

Width to test

Expected gallery

Mobile

375px

1 column

Tablet

768px

2 columns

Desktop

1440px

3 columns

6. Screenshots for submission
You need to capture the screenshots yourself in Chrome, because they must show your actual running webpage.

Gallery - 2 columns of Images for desktop gallery and 1 column for mobile - Need code that works - Images & Videos - Squarespace Forum
Screenshot 1: mobile.png

Set the viewport to 375px wide and capture the page with the one-column gallery visible.

Squarespace Avenue Template
Screenshot 2: tablet.png

Set the viewport to 768px wide and capture the two-column gallery.

Projects 8 - Three-column filterable gallery with overlays - Shadcnblocks.com
Screenshot 3: desktop.png

Set the viewport to 1440px wide and capture the three-column gallery.

Save each screenshot in your screenshots folder using the filenames above.

7. Assignment report
You can include this report with your submission.

Writing


Assignment 9.1 — Convert a Desktop Page into a Mobile-First Layout
Objective: To convert a webpage into a responsive layout using mobile-first CSS and media queries.

Tools Used: HTML5, CSS3, Google Chrome DevTools.

Implementation:

Added the viewport meta tag to the HTML document.
Created a responsive photo gallery using HTML and CSS.
Applied mobile-first styling with a single-column layout.
Added a breakpoint at 600px for tablet screens.
Added a breakpoint at 1024px for desktop screens.
Used CSS Grid and Flexbox to arrange the gallery and navigation.
Used responsive images, box-sizing: border-box, and flexible containers to prevent horizontal overflow.
Tested the layout at mobile, tablet, and desktop viewport sizes.
Result: The webpage adapts to different screen sizes. Mobile devices display one column, tablets display two columns, and desktops display three columns. The responsive design improves usability and readability across devices.

Conclusion: The assignment demonstrates the implementation of a mobile-first responsive webpage using HTML, CSS Grid, Flexbox, and media queries.

Final submission checklist

index.html

style.css

screenshots/mobile.png

screenshots/tablet.png

screenshots/desktop.png

Assignment report
Note: The HTML and CSS above are the completed code for the assignment. Before submitting, run the page and verify that all images load and that there is no horizontal scrolling at the three test widths.


You said:

name=Assignment-9.2.md Assignment 9.2 — Responsive Typography & Images[cite: 42] What to build: A webpage where text and images adjust properly across different screen sizes[cite: 42]. Steps:

Create an article or portfolio page[cite: 42].
Add headings, paragraphs, and images[cite: 42].
Use rem, em, or clamp() for font sizes[cite: 42].
Apply max-width: 100% and height: auto to images[cite: 42].
Set a suitable max-width on the content container[cite: 42].
Improve line length and spacing for mobile and desktop[cite: 42].
Check that images do not stretch and text does not overflow the screen[cite: 42]. Submission: Responsive webpage and mobile/desktop screenshots[cite: 42]. assignment solve  it

ChatGPT said:
