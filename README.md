# imazilla
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>IMAZILLA Layout</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: black;
      font-family: Arial, sans-serif;
      color: white;
    }

    /* Top Navbar */
    .container {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 20px;
      background-color: #111;
      box-shadow: 0 2px 5px rgba(255, 255, 255, 0.1);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .d1 {
      display: grid;
      grid-template-rows: 7px 7px 7px;
      row-gap: 5px;
      height: 25px;
      width: 30px;
      justify-items: center;
      align-items: center;
      cursor: pointer;
    }

    .d10, .d11, .d12 {
      background-color: white;
      height: 4.5px;
      width: 25px;
      border-radius: 2px;
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
      margin-right: auto;
      margin-left: 10px;
      color: white;
    }

    .d2 {
      flex-grow: 1;
      margin: 0 20px;
    }

    .input {
      width: 100%;
      padding: 8px 12px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 8px;
      outline: none;
    }

    .input:focus {
      border-color: #007BFF;
    }

    .Create {
      border: solid grey 2px;
      background-color: grey;
      border-radius: 20px;
      width: 100px;
      height: 35px;
      color: white;
      font-weight: bold;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 20px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .Create:hover {
      background-color: #555;
    }

    .bell {
      font-size: 24px;
      margin: 0 20px;
      cursor: pointer;
      transition: color 0.3s;
    }

    .bell:hover {
      color: #007BFF;
    }

    .d3 {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      overflow: hidden;
      border: 2px solid #ccc;
      cursor: pointer;
    }

    .image {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
    }

    /* Main Content Layout */
    .main-content {
      display: flex;
      padding: 20px;
      gap: 20px;
    }

    /* Sidebar */
    .main1 {
      background-color: #222;
      border: solid white 2px;
      width: 250px;
      border-radius: 10px;
      padding: 20px 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      transition: background-color 0.3s, transform 0.3s;
    }

    .main1 div {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      font-size: 18px;
      border-bottom: 1px solid #333;
      cursor: pointer;
      transition: background-color 0.3s, transform 0.3s;
    }

    .main1 div:hover {
      background-color: #333;
      transform: scale(1.05);
      border-radius: 10px;
    }

    /* Grid of Boxes */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      flex-grow: 1;
    }

    .grid div {
      background-color: #222;
      border: solid black 2px;
      border-radius: 10px;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
    }

    .grid div:hover {
      background-color: #333;
      transform: scale(1.05);
      box-shadow: 0 4px 8px rgba(255, 255, 255, 0.2);
    }

    .image1 {
      height: 250px;
      width: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .grid div:hover .image1 {
      transform: scale(1.1);
    }

    .grid p {
      margin: 10px 0;
      font-size: 16px;
    }

    /* Sidebar Hidden Class */
    .hidden-sidebar {
      display: none !important;
    }
  </style>
</head>
<body>

  <!-- Top Navbar -->
  <div class="container">
    <div class="d1" title="Toggle Sidebar">
      <div class="d10"></div>
      <div class="d11"></div>
      <div class="d12"></div>
    </div>

    <p class="logo">IMAZILLA</p>

    <div class="d2">
      <input type="search" id="gsearch" name="gsearch" placeholder="Search..." class="input">
    </div>

    <div class="Create" title="Click to Create New">+Create</div>
    <div class="bell" title="Notifications">🔔</div>
    <div class="d3" title="Your Profile">
      <img src="shivam's image.jpg" alt="profile" class="image">
    </div>
  </div>

  <!-- Main Content -->
  <div class="main-content">
    <!-- Sidebar -->
    <div class="main1">
      <div>Home</div>
      <div>Trending</div>
      <div>Wishlist</div>
      <div>Saved</div>
      <div>Like</div>
      <div>Buy</div>
      <div>Rating</div>
      <div>Logout</div>
    </div>

    <!-- Grid -->
    <div class="grid">
      <div><img src="yoga 4.jpg" alt="Yoga Pose 1" class="image1"><p>Image 1</p></div>
      <div><img src="yoga1.jpg" alt="Yoga Pose 2" class="image1"><p>Image 2</p></div>
      <div><img src="yoga2.jpg" alt="Yoga Pose 3" class="image1"><p>Image 3</p></div>
      <div><img src="yoga3.jpg" alt="Yoga Pose 4" class="image1"><p>Image 4</p></div>
      <div><img src="yoga6.avif" alt="Yoga Pose 5" class="image1"><p>Image 5</p></div>
      <div><img src="yoga7.webp" alt="Yoga Pose 6" class="image1"><p>Image 6</p></div>
      <div><img src="yoga.avif" alt="Yoga Pose 7" class="image1"><p>Image 7</p></div>
      <div><img src="KM-Diverse-Group.webp" alt="Yoga Group" class="image1"><p>Image 8</p></div>
      <div><img src="s.webp" alt="Yoga Session" class="image1"><p>Image 9</p></div>
      <div><img src="iuygfghxc.avif" alt="Stretching" class="image1"><p>Image 10</p></div>
      <div><img src="p.jpg" alt="Meditation" class="image1"><p>Image 11</p></div>
      <div><img src="concentrated-young-woman-with-flexible-body.jpg" alt="Forward Bend Pose" class="image1"><p>Image 12</p></div>
    </div>
  </div>

  <!-- JavaScript -->
  <script>
    // Toggle Sidebar
    const burgerMenu = document.querySelector('.d1');
    const sidebar = document.querySelector('.main1');

    burgerMenu.addEventListener('click', () => {
      sidebar.classList.toggle('hidden-sidebar');
    });

    // Search input
    const searchInput = document.querySelector('#gsearch');
    searchInput.addEventListener('input', (e) => {
      console.log('Searching for:', e.target.value);
    });

    // Create button
    const createButton = document.querySelector('.Create');
    createButton.addEventListener('click', () => {
      alert('Create button clicked!');
    });

    // Bell icon
    const bellIcon = document.querySelector('.bell');
    bellIcon.addEventListener('click', () => {
      alert('Notifications clicked!');
    });

    // Profile click
    const profile = document.querySelector('.d3');
    profile.addEventListener('click', () => {
      alert('Profile clicked!');
    });

    // Tooltips + click events on image cards
    const gridImages = document.querySelectorAll('.grid div');
    gridImages.forEach((card, index) => {
      card.setAttribute('title', `Click to view more about Image ${index + 1}`);
      card.addEventListener('click', () => {
        alert(`You clicked on Image ${index + 1}`);
      });
    });
  </script>

</body>
</html>
