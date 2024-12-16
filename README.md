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
HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THE GOATS GALLERY</title>
    <style>
        body {
            background: url('c:/Users/admin/Downloads/cristiano-ronaldo-1920x1080-14055.png') no-repeat center center fixed;
            background-size: cover;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        
        }
        

        .title {
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 42px;
            background-color: rgb(0, 0, 0);
            color: rgb(255, 255, 255);
            z-index: 1;
            text-shadow: 2px 2px 4px rgb(255, 255, 255) ;
            font-style: oblique;
            padding: 30;
        }

        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
            width: 100%;
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgb(33, 229, 255);
            transition: transform 0.3s ease;
        }

        .gallery-item img:hover {
            transform: scale(1.3);
            cursor: pointer;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            padding-top: 100px;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.7);
        }

        .modal-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 800px;
            border-radius: 10px;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 25px;
            color: #ffffff;
            font-size: 36px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: #ccc;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="title">THE GOATS GALLERY</div>
    <div class="gallery-container">
        <div class="gallery-item">
            <img src="c:\Users\admin\Downloads\wp2707698.webp" alt="Cristiano Ronaldo Wallpaper 1">
        </div>
        <div class="gallery-item">
            <img src="c:\Users\admin\Downloads\Ronaldo wallpaper.jpg" alt="Cristiano Ronaldo Wallpaper 2">
        </div>
        <div class="gallery-item">
            <img src="c:\Users\admin\Downloads\wallpaper_cristiano_ronaldo___real_madrid_2017_by_thiagojustino_dbk0bp7.png" alt="Cristiano Ronaldo Wallpaper 3">
        </div>
        <div class="gallery-item">
            <img src="c:\Users\admin\Downloads\100137-1920x1080-desktop-full-hd-cristiano-ronaldo-wallpaper-image.jpg" alt="Cristiano Ronaldo Wallpaper 4">
        </div>
        <div class="gallery-item">
            <img src="c:\Users\admin\Downloads\wp11906341.jpg" alt="Cristiano Ronaldo Wallpaper 5">
        </div>
        <div class="gallery-item">
          <img src="c:\Users\admin\Downloads\wp4717587.jpg" alt="Cristiano Ronaldo Wallpaper 5">
      </div>
      <div class="gallery-item">
        <img src="c:\Users\admin\Downloads\cr7-cool-fade-red-4tuspkxk42buyr4c.jpg" alt="Cristiano Ronaldo Wallpaper 5">
      </div>
      <div class="gallery-item">
        <img src="c:\Users\admin\Downloads\unnamed (1).jpg" alt="Cristiano Ronaldo Wallpaper 5">
      </div>
    </div>

    <div class="modal" id="modal">
        <span class="close" id="close">&times;</span>
        <img class="modal-content" id="modal-img">
    </div>

    <script>
        const images = document.querySelectorAll('.gallery-item img');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        const closeBtn = document.getElementById('close');

        images.forEach((image) => {
            image.addEventListener('click', () => {
                modal.style.display = 'block';
                modalImg.src = image.src; 
            });
        });

        closeBtn.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        window.addEventListener('click', (event) => {
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>
</html>

```

# OUTPUT:
![Screenshot 2024-12-16 152302](https://github.com/user-attachments/assets/4f6cc059-5e2d-4eb7-94bc-4ca9e91b1c7f)
![Screenshot 2024-12-16 152222](https://github.com/user-attachments/assets/4a9cf692-a301-4ae1-b6ee-b8c73c43dee3)
![Screenshot 2024-12-16 152243](https://github.com/user-attachments/assets/ae084fae-e731-404c-9a24-5c588f7e6c6c)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
