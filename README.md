# Ex.08 Design of Interactive Image Gallery
## Date:15-05-2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Harry Potter Gallery</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background: #0b1220 url('castle.webp') no-repeat center center fixed;
            background-size: cover;
            color: #ffffff;
        }

        h1 {
            margin-top: 20px;
            font-size: 3rem;
            text-shadow: 0 0 10px #9b7653;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }

        .gallery img {
    width: 490px;
    height: 680px; 
    border: 4px solid #9b7653;
    border-radius: 12px;
    cursor: pointer;
    object-fit: cover;
    transition: transform 0.3s, box-shadow 0.3s;
    box-shadow: 0 0 5px #e0c097;
}

        .gallery img:hover {
            transform: scale(1.1);
            box-shadow: 0 0 20px #c9a75a;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background-color: rgba(11, 18, 32, 0.9);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border: 5px solid #4e4339;
            border-radius: 15px;
            box-shadow: 0 0 30px #121211;
        }

        .modal span {
            position: absolute;
            top: 25px;
            right: 40px;
            font-size: 40px;
            color: #c9a75a;
            cursor: pointer;
            font-weight: bold;
            text-shadow: 0 0 8px #c9a75a;
        }
    </style>
</head>
<body>
    <h1>The Vault of Wizarding World</h1>

    <div class="gallery">
        <img src="hermoine.jpg" alt="Hermione Granger" onclick="openModal(this)">
        <img src="draco.jpg" alt="Draco Malfoy" onclick="openModal(this)">
        <img src="hh.jpg" alt="Harry Potter and Hedwig" onclick="openModal(this)">
        <img src="dobby.jpg" alt="Dobby" onclick="openModal(this)">
        <img src="ron.jpg" alt="Ron Weasley" onclick="openModal(this)">
        <img src="dms.jpg" alt="Trio" onclick="openModal(this)">
        <img src="twins.jpg" alt="Hagrid" onclick="openModal(this)">
        <img src="tom.jpg" alt="Hagrid" onclick="openModal(this)">
        <img src="sl.jpg" alt="Hagrid" onclick="openModal(this)">
        <img src="hag.webp" alt="Hagrid" onclick="openModal(this)">
    </div>

    <div class="modal" id="imageModal">
        <span onclick="closeModal()">&times;</span>
        <img id="modalImage" src="" alt="Harry Potter Image" />
    </div>

    <script>
        function openModal(image) {
            const modal = document.getElementById('imageModal');
            const modalImg = document.getElementById('modalImage');
            modal.style.display = 'flex';
            modalImg.src = image.src;
            modalImg.alt = image.alt;
        }

        function closeModal() {
            document.getElementById('imageModal').style.display = 'none';
        }
    </script>
</body>
</html>
```
## OUTPUT:
![alt text](<images/galleryapp/static/Screenshot 2025-05-15 142417.png>)
![alt text](<images/galleryapp/static/Screenshot 2025-05-15 142427.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
