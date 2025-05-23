# Ex.08 Design of Interactive Image Gallery
## Date:
25/04/2025

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
  <title>Disney Princesses</title>
  <style>
    body {
      font-family: 'Comic Sans MS', cursive, sans-serif;
      margin: 0;
      padding: 0;
      background: url("background.jpg") no-repeat center center fixed;
      background-size: cover;
      color: #880044;
    }

    h1 {
      text-align: center;
      margin: 20px 0;
      font-size: 3em;
      color: #cc0066;
      text-shadow: 2px 2px 6px #fff;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
      padding: 20px;
    }

    .gallery img {
      width: 220px;
      height: 220px;
      object-fit: cover;
      border-radius: 50%;
      border: 4px solid white;
      box-shadow: 0 4px 12px rgba(0,0,0,0.5);
      transition: transform 0.3s;
      cursor: pointer;
    }

    .gallery img:hover {
      transform: scale(1.1);
    }

    .princess-name {
      text-align: center;
      margin-top: 8px;
      font-weight: bold;
      color: #cc3399;
    }

    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.9);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .modal img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
      border: 5px solid white;
    }

    .modal-close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 40px;
      color: white;
      cursor: pointer;
    }

    .card {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  </style>
</head>
<body>

  <h1>Which Disney Princess Are You?</h1>

  <div class="gallery">
    <div class="card"><img src="tiana.png" alt="Tiana"><div class="princess-name">Tiana</div></div>
    <div class="card"><img src="snowwhite.png" alt="Snow White"><div class="princess-name">Snow White</div></div>
    <div class="card"><img src="rapunzel.png" alt="Rapunzel"><div class="princess-name">Rapunzel</div></div>
    <div class="card"><img src="pocahontas.png" alt="Pocahontas"><div class="princess-name">Pocahontas</div></div>
    <div class="card"><img src="mulan.png" alt="Mulan"><div class="princess-name">Mulan</div></div>
    <div class="card"><img src="merida.png" alt="Merida"><div class="princess-name">Merida</div></div>
    <div class="card"><img src="jasmine.png" alt="Jasmine"><div class="princess-name">Jasmine</div></div>
    <div class="card"><img src="cinderalle.png" alt="Cinderella"><div class="princess-name">Cinderella</div></div>
    <div class="card"><img src="bella.png" alt="Belle"><div class="princess-name">Belle</div></div>
    <div class="card"><img src="aurora.png" alt="Aurora"><div class="princess-name">Aurora</div></div>
    <div class="card"><img src="arial.png" alt="Ariel"><div class="princess-name">Ariel</div></div>
  </div>

  <div class="modal" id="imageModal" role="dialog" aria-modal="true" tabindex="-1">
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
        modalImage.alt = img.alt;
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

    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') {
        modal.style.display = 'none';
      }
    });
  </script>

</body>
</html>

```
## OUTPUT:

![alt text](1st.png)
![alt text](<Screenshot (66).png>)
![alt text](<Screenshot (67).png>)
![alt text](<Screenshot (68).png>)
![alt text](<Screenshot (69).png>)
![alt text](<Screenshot (70).png>)
![alt text](<Screenshot (71).png>)
![alt text](<Screenshot (72).png>)
![alt text](<Screenshot (73).png>)
![alt text](<Screenshot (74).png>)
![alt text](<Screenshot 2025-05-12 143520.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
