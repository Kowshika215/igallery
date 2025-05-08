# Ex.08 Design of Interactive Image Gallery
## Date:

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
<html>
<head>
  <title>Interactive image gallery</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      background: #BEE4D0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .mainbox {
      width: 80%;
      max-width: 800px;
      border: 2px solid #6F826A;
      height: 500px;
      overflow: hidden;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.5);
      position: relative;
    }

    .images {
      display: flex;
      width: 100%;
      transition: transform 0.5s ease-in-out;
    }

    .slide {
      min-width: 100%;
      height: 100%;
    }

    .slide img {
      width: 100%;
      max-width: 800px;
      height: 500px;
      object-fit: cover;
    }

    .button {
      top: 50%;
      position: absolute;
      transform: translateY(-50%);
      background: rgba(255, 255, 255, 0.3);
      border: none;
      font-size: 2rem;
      color: #EDE8DC;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 50%;
      transition: background 0.3s;
      z-index: 2;
    }

    .button:hover {
      background: rgba(255, 255, 255, 0.6);
    }

    .left {
      left: 15px;
    }

    .right {
      right: 15px;
    }
    .txtup, .text-bottom {
      width: 80%;
      max-width: 700px;
      text-align: center;
      font-family: Arial, sans-serif;
      margin: 10px 0;
    }

    .txt-up {
      font-weight:bolder;
      color:#143D60;
    }

    .txt-down{
      margin-top: 7px;
      font-weight:bold;
      line-height: 25px;
      color:#27667B;
    }

  </style>
</head>
<body>
  <div class="txt-up"><h1>Interactive image gallery</h1></div>
  <div class="mainbox">
    <div class="images" id="images">
      <div class="slide"><img src="virat.webp" alt="img1"></div>
      <div class="slide"><img src="rohit.avif" alt="img2"></div>
      <div class="slide"><img src="iyer.webp" alt="img3"></div>
      <div class="slide"><img src="msd.jpg" alt="img4"></div>
      <div class="slide"><img src="Rahul.webp" alt="img5"></div>
    </div>
    <button class="button left" id="left"><</button>
    <button class="button right" id="right">></button>

  <script>
    const slider = document.getElementById('images');
    const slides = document.querySelectorAll('.slide');
    const left_bt = document.getElementById('left');
    const right_bt = document.getElementById('right');
    let currentIndex = 0;

    function updateSlider() {
      slider.style.transform = `translateX(-${currentIndex * 100}%)`;
    }

    function nextSlide() {
      currentIndex = (currentIndex + 1) % slides.length;
      updateSlider();
    }

    function prevSlide() {
      currentIndex = (currentIndex - 1 + slides.length) % slides.length;
      updateSlider();
    }

    right_bt.addEventListener('click', nextSlide);
    left_bt.addEventListener('click', prevSlide);
    right_bt.addEventListener('mouseenter', nextSlide);
    left_bt.addEventListener('mouseenter', prevSlide);
  </script>
</body>
</html>
```

## OUTPUT:

![Screenshot 2025-05-08 090217](https://github.com/user-attachments/assets/22bf7ba4-f111-4b4d-ae67-ba38932f4d47)
![Screenshot 2025-05-08 090225](https://github.com/user-attachments/assets/45468482-ab44-487c-9b1e-72f4ad92080c)
![Screenshot 2025-05-08 090233](https://github.com/user-attachments/assets/2a4c6bd8-c2bf-4c4d-ab5e-faae277933bd)
![Screenshot 2025-05-08 090244](https://github.com/user-attachments/assets/632f3824-723b-4c03-9d96-f295289973fd)
![Screenshot 2025-05-08 090251](https://github.com/user-attachments/assets/17d6da02-129a-4465-b82a-116efe369bbc)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
