# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HOUSES OF HOGWARTS</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            padding: 20px;
        }
        .gallery img {
            width: 200px;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .gallery img:hover {
            transform: scale(1.1);
        }
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }
        .modal img {
            max-width: 90%;
            max-height: 80%;
            border-radius: 10px;
        }
        .modal-close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 30px;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body>

<h1 style="text-align: center; margin-top: 20px;">HOGWARTS</h1>
<div class="gallery">
    <img src=img1.png alt="Image 1">
    <img src=img2.png alt="Image 2">
    <img src=img3.jpg alt="Image 3">
    <img src=img4.png alt="Image 4">
    <img src=img5.png alt="Image 5">
</div>

<div class="modal" id="imageModal">
    <span class="modal-close" id="closeModal">&times;</span>
    <img src="" alt="Expanded View" id="modalImage">
</div>

<script>
    const galleryImages = document.querySelectorAll('.gallery img');
    const modal = document.getElementById('imageModal');
    const modalImage = document.getElementById('modalImage');
    const closeModal = document.getElementById('closeModal');

    galleryImages.forEach(img => {
        img.addEventListener('click', () => {
            modal.style.display = 'flex';
            modalImage.src = img.src;
        });
    });

    closeModal.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });
</script>

</body>
</html>
```
# OUTPUT:
![447350983-15bdf0e0-0c72-4d45-9536-86e7b64e734e](https://github.com/user-attachments/assets/a565160d-0edf-491c-a4d8-8cf683e325c4)

![447351027-1e5fe967-01f2-4e69-a282-912205d1e37a](https://github.com/user-attachments/assets/33d83c40-433b-4e0f-9570-3d2846cc49a3)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
