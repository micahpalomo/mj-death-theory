# Recreate the base directory for the updated website with more details, photos, and narratives
import os
import shutil

base_dir_v3 = "/mnt/data/mj_fan_theories_site_v3"
os.makedirs(base_dir_v3, exist_ok=True)

# Updated index.html with more details
index_html_v3 = """<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Michael Jackson Fan Theories</title>
    <link rel="stylesheet" href="style.css">
    <script defer src="script.js"></script>
</head>
<body>
    <header>
        <h1>Michael Jackson: The Theories</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="theories.html">Theories</a></li>
                <li><a href="evidence.html">Evidence</a></li>
                <li><a href="about.html">About</a></li>
            </ul>
        </nav>
    </header>
    <section class="intro">
        <h2>Did Michael Jackson Really Die?</h2>
        <p>Explore the most talked-about fan theories surrounding the King of Pop’s mysterious passing.</p>
        <img src="images/mj_home.jpg" alt="Michael Jackson" class="featured-image">
        <button id="explore-btn">Explore Theories</button>
    </section>
</body>
</html>
"""

# Updated style.css with image styling
style_css_v3 = """body {
    font-family: 'Arial', sans-serif;
    background-color: #000;
    color: #fff;
    margin: 0;
    padding: 0;
    text-align: center;
}
header {
    background-color: #222;
    padding: 20px;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
}
h1 {
    color: gold;
}
nav ul {
    list-style-type: none;
    padding: 0;
}
nav ul li {
    display: inline;
    margin: 0 15px;
}
nav ul li a {
    color: white;
    text-decoration: none;
}
.intro {
    padding: 100px 20px;
    margin-top: 80px;
}
button {
    background-color: gold;
    color: black;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    transition: transform 0.2s ease-in-out;
}
button:hover {
    transform: scale(1.1);
}
.featured-image {
    width: 80%;
    max-width: 500px;
    margin-top: 20px;
    border-radius: 10px;
}
"""

# Updated script.js with enhanced interactivity
script_js_v3 = """document.getElementById('explore-btn').addEventListener('click', function() {
    alert('Redirecting to Theories page...');
    window.location.href = 'theories.html';
});"""

# Updated theories.html with more details and images
theories_html_v3 = """<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Theories</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>The Theories</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="theories.html">Theories</a></li>
                <li><a href="evidence.html">Evidence</a></li>
                <li><a href="about.html">About</a></li>
            </ul>
        </nav>
    </header>
    <section class="content">
        <h2>Popular Theories</h2>
        <article>
            <h3>Michael Jackson Faked His Death</h3>
            <img src="images/mj_fake_death.jpg" alt="Michael Jackson Theory" class="featured-image">
            <p>Some fans believe MJ staged his death to escape the pressures of fame. Reports of sightings and hidden messages in his music fuel this theory.</p>
        </article>
        <article>
            <h3>Involvement of Dr. Conrad Murray</h3>
            <img src="images/mj_conrad_murray.jpg" alt="Dr. Conrad Murray" class="featured-image">
            <p>Dr. Conrad Murray was convicted of involuntary manslaughter, but many suspect there was more to the story, possibly a cover-up.</p>
        </article>
    </section>
</body>
</html>
"""

# Updated evidence.html with more narratives
evidence_html_v3 = """<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Evidence</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Evidence</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="theories.html">Theories</a></li>
                <li><a href="evidence.html">Evidence</a></li>
                <li><a href="about.html">About</a></li>
            </ul>
        </nav>
    </header>
    <section class="content">
        <h2>Supporting and Debunking Theories</h2>
        <p>Investigators have examined multiple clues, from medical reports to surveillance footage, to uncover the truth.</p>
        <img src="images/mj_evidence.jpg" alt="Michael Jackson Evidence" class="featured-image">
    </section>
</body>
</html>
"""

# Updated about.html with more background
about_html_v3 = """<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>About This Site</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="theories.html">Theories</a></li>
                <li><a href="evidence.html">Evidence</a></li>
                <li><a href="about.html">About</a></li>
            </ul>
        </nav>
    </header>
    <section class="content">
        <h2>Why This Website Exists</h2>
        <p>This site was created to explore and discuss fan theories surrounding Michael Jackson’s death, providing an open platform for discussion.</p>
    </section>
</body>
</html>
"""

# Create an images directory and add placeholders
images_dir_v3 = os.path.join(base_dir_v3, "images")
os.makedirs(images_dir_v3, exist_ok=True)

# Placeholder image paths (real images would need to be uploaded manually)
image_files_v3 = {
    "mj_home.jpg": "Michael Jackson homepage image placeholder",
    "mj_fake_death.jpg": "Image representing the fake death theory",
    "mj_conrad_murray.jpg": "Dr. Conrad Murray's involvement",
    "mj_evidence.jpg": "Evidence supporting and debunking theories"
}

# Writing files
files_v3 = {
    "index.html": index_html_v3,
    "style.css": style_css_v3,
    "script.js": script_js_v3,
    "theories.html": theories_html_v3,
    "evidence.html": evidence_html_v3,
    "about.html": about_html_v3
}

for filename, content in files_v3.items():
    with open(os.path.join(base_dir_v3, filename), "w") as file:
        file.write(content)

# Create a zip file
zip_path_v3 = "/mnt/data/mj_fan_theories_site_v3.zip"
shutil.make_archive(zip_path_v3.replace(".zip", ""), "zip", base_dir_v3)

zip_path_v3
