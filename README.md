<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Slider</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.rtl.min.css" 
  integrity="sha384-gXt9imSW0VcJVHezoNQsP+TNrjYXoGcrqBZJpry9zJt8PCQjobwmhMGaDHTASo9N" crossorigin="anonymous">
  <script defer src="https://cdn.jsdelivr.net/npm/alpinejs@3.15.0/dist/cdn.min.js"></script>
 <link rel="stylesheet" href="index.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.13.1/font/bootstrap-icons.min.css">
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  </style>
  
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, sans-serif;
      background: #f5f5f5;
    }

    .slider {
      position: relative;
      width: 100%;
      max-width: 2200px;
      margin: 0 auto;
      height: 120vh;
      background: #f5f5f5;
      box-shadow: 0 30px 50px #dbdbdb;
      overflow: hidden;
      transition: all 03.ms;
    
    }

    .slide {
      position: relative;
      width: 100%;
      height: 100%;
      transform: scale(30.3s);
    }

    .slide .item {
      width: 200px;
      height: 250px;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      box-shadow: 0 30px 40px #50505060;
      background-position: center;
      background-size: cover;
      transition: all 0.5s;
    }

    .slide .item:nth-child(1),
    .slide .item:nth-child(2) {
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      transform: none;
    }

    .slide .item:nth-child(3) {
      left: 50%;
    }

    .slide .item:nth-child(4) {
      left: calc(50% + 220px);
    }

    .slide .item:nth-child(5) {
      left: calc(50% + 440px);
    }

    .slide .item:nth-child(n + 6) {
      opacity: 0;
      pointer-events: none;
    }

    .item .contents {
      position: absolute;
      top: 50%;
      left: 10%;
      width: 80%;
      color: #fff;
      text-shadow: 0 2px 10px #0008;
      transform: translateY(-50%);
      display: none;
    }

    .slide .item:nth-child(2) .contents {
      display: block;
    }

    .contents .name {
      font-size: 3vw;
      text-transform: uppercase;
      font-weight: bold;
      opacity: 0;
      animation: animate 1s ease-in-out forwards;
    }

    .contents .des {
      margin-top: 1vw;
      margin-bottom: 2vw;
      font-size: 1.2vw;
      line-height: 1.5;
      opacity: 0;
      animation: animate 1s ease-in-out 0.3s forwards;
    }

    .contents button {
      padding: 0.8em 1.6em;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      background: rgba(129, 129, 129, 0.582);
      color: #000;
      font-size: 1em;
      transition: all 0.3s;
      opacity: 0;
      animation: animate 1s ease-in-out 0.6s forwards;
    }

    .contents button:hover {
      background: #6b6969;
      transform: scale(1.05);
    }

    @keyframes animate {
      from {
        opacity: 0;
        transform: translateY(50px);
        filter: blur(10px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
        filter: blur(0);
      }
    }

    .button {
      display: flex;
      justify-content: center;
      gap: 20px;
      position: absolute;
      bottom: 20px;
      width: 100%;
    }

    .button button {
      width: 40px;
      height: 40px;
      border-radius: 10px;
      border: 2px solid #0008;
      background: rgba(255, 255, 255, 0.7);
      cursor: pointer;
      transition: 0.3s;
    }

    .button button:hover {
      transform: scale(1.1);
      background: #fff;
    }

    /* ======= 📱 Responsive ======= */
    @media (max-width: 992px) {
      .slider {
        height: 100vh;
        border-radius: 0;
      }

      .slide .item {
        width: 100%;
        height: 100%;
        left: 0 !important;
        top: 0 !important;
        transform: none !important;
        border-radius: 0;
      }

      .slide .item:nth-child(n + 3) {
        display: none;
      }

      .item .contents {
        width: 90%;
        left: 5%;
        text-align: center;
      }

      .contents .name {
        font-size: 6vw;
      }

      .contents .des {
        font-size: 3.5vw;
      }

      .contents button {
        font-size: 3.5vw;
      }

      .button {
        bottom: 10px;
      }
    }

    @media (max-width: 576px) {
      .slider {
        height: 100vh;
      }

      .contents .name {
        font-size: 6vw;
      }

      .contents .des {
        font-size: 4vw;
      }

      .contents button {
        font-size: 4vw;
        padding: 8px 16px;
      }
    }

    /* header */
    body {
    font-family: "Poppins", sans-serif;
    background: #f5f5f5;
  }

  /* Navbar */
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    body {
      background-color: #000;
      color: #fff;
    }

    /* Main navbar */
    nav {
      width: 100%;
      background-color: #00000046;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 12px 40px;
      position: fixed;
      top: 0;
      z-index: 1000;
    }

    .logo {
      color: white;
      font-size: 24px;
      font-weight: bold;
      cursor: pointer;
    }

    .nav-links {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      font-size: 16px;
      padding: 6px 18px;
      border-radius: 5px;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: white;
      background-color: #222;
    }

    .nav-links a.active {
      color: white;
      border-bottom: 2px solid #fff;
    }

    .search-box {
      position: relative;
    }

    .search-box .input1 {
      padding: 6px 30px 6px 10px;
      border: none;
      border-radius: 20px;
      outline: none;
      background-color: #ffffffc4;
    }

    .search-box button {
      position: absolute;
      right: 5px;
      top: 3px;
      background: none;
      border: none;
      color: #555;
      cursor: pointer;
      font-size: 16px;
    }

    /* Hamburger icon */
    .menu-icon {
      display: none;
      font-size: 26px;
      cursor: pointer;
      color: white;
    }

    /* Mobile menu overlay */
    .mobile-menu {
      position: fixed;
      top: 0;
      left: 0;
      height: 100vh;
      width: 100%;
      background: linear-gradient(to right,rgb(0, 0, 0),rgb(44, 43, 43), rgb(2, 2, 2));
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 30px;
      transform: translateX(-100%);
      transition: 0.4s ease;
      z-index: 99;
    }

    .mobile-menu.active {
      transform: translateX(0);
    }

    .mobile-menu a {
      color: #ffffff;
      font-size: 26px;
      text-decoration: none;
      transition: 0.3s;
      border-bottom: 1px solid #444;
      padding-bottom: 8px;
    }

    .mobile-menu a:hover {
      color: white;
    }

    .close-icon {
  position: absolute;
  top: 70px;
  right: 25px;
  font-size: 38px;
  color: #f8f8f8;
  cursor: pointer;
}

    /* Responsive */
    @media (max-width: 900px) {
      .nav-links, .search-box {
        display: none;
      }
      .menu-icon {
        display: block;
      }
    }
/* footer */
* {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
     
    }

    
    footer {
      background:black;
      color: #fff;
      padding: 40px 20px;
      box-shadow: inset -1px -1px 15px 11px #958a8a !important;
    }

    .footer-container {
      max-width: 1200px;
      margin: auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 40px;
    }

    .footer-section {
      flex: 1 1 220px;
      min-width: 200px;
    }

    .footer-section h3 {
      margin-bottom: 15px;
      font-size: 16px;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: #ffffff; /* رنگ طلایی-خاکی */
    }

    .footer-section ul {
      list-style: none;
    }

    .footer-section ul li {
      margin-bottom: 8px;
    }

    .footer-section ul li a {
      color: #ffffff;
      text-decoration: none;
      transition: color 0.3s;
    }

    .footer-section ul li a:hover {
      color: #8b8b88;
    }

    .payment-logos img {
      width: 45px;
      margin: 5px;
      filter: brightness(0) invert(1);
    }

    .social-icons a {
      color: #fff;
      margin-right: 12px;
      font-size: 20px;
      text-decoration: none;
      transition: color 0.3s;
    }

    .social-icons a:hover {
      color: #8b8b88;
    }

    .newsletter {
      display: flex;
      flex-direction: column;
      margin-top: 10px;
    }

    .newsletter p {
      font-size: 14px;
      margin-bottom: 10px;
      color: #ddd;
    }

    .newsletter input[type="email"] {
      padding: 10px;
      border: 1px solid #fff;
      border-radius: 3px;
      margin-bottom: 10px;
      background-color: #000;
      color: #fff;
      outline: none;
    }

    .newsletter button {
      background-color: #000;
      color: #fff;
      border: 1px solid #fff;
      padding: 10px;
      cursor: pointer;
      transition: all 0.3s;
    }

    .newsletter button:hover {
      background-color:#5a5a58;
      border-color: #42424179;
      color: #000;
    }

    .footer-bottom {
      text-align: center;
      margin-top: 30px;
      font-size: 14px;
      color: #8b8b88;
    }

    @media (max-width: 768px) {
      .footer-container {
        flex-direction: column;
        text-align: center;
      }
      .social-icons {
        justify-content: center;
      }
    }

  </style>
</head>
<body>

   <!-- header -->
   <nav>
    <div class="container">
     <div class="row">
      <div class="col-lg-3 ">
        <div class="logo"><img class="w-50 h-50" src="../porject-bootstrap.4/Annotation 2025-11-02 080054.png" alt=""></div>
       </div>
 
      <div class="col-lg-7">
       <div class="nav-links">
         <a href="index.html"   class="active">Home</a>
         <a href="about.html">About</a>
         <a href="services.html">Services</a>
         <a href="Portfolio.html">Portfolio</a>
         <a href="pricing.html">Pricing</a>
         <a href="team.html">Team</a>
         <a href="blog.html">Blog</a>
         <a href="contact.html">Contact</a>
       </div>
   
      </div>
     </div>
    </div>
    
 
     <div class="menu-icon" onclick="openMenu()">☰</div>
   </nav>
 
   <!-- Mobile Menu -->
 <div class="mobile-menu" id="mobileMenu">
     <div class="close-icon" onclick="closeMenu()">×</div> <!-- ⬅️ این خط را اضافه کن -->
     <a href="index.html">Home</a>
     <a href="about.html">About</a>
     <a href="services.html">Services</a>
     <a href="Portfolio.html">Portfolio</a>
     <a href="pricing.html">Pricing</a>
     <a href="team.html">Team</a>
     <a href="blog.html">Blog</a>
     <a href="contact.html">Contact</a>
   </div>

  

<!-- home -->
  <div class="slider">
    <div class="slide">
      <div class="item" style="background-image:url('img-black\ \(4\).png');">
        <div class="contents">
          <div class="name"> Necklace</div>
          <div class="des">Life is like riding a bicycle. To keep your balance, you must keep moving.</div>
          <button>See More</button>
        </div>
      </div>

      <div class="item" style="background-image:url('img-black\ \(7\).png');">
        <div class="contents">
          <div class="name">Bracelet</div>
          <div class="des">You must be the change you wish to see in the world</div>
          <button>See More</button>
        </div>
      </div>

      <div class="item" style="background-image:url('img-black\ \(8\).png');">
        <div class="contents">
          <div class="name">Rings</div>
          <div class="des">Always remember that you are absolutely unique. Just like everyone else</div>
          <button>See More</button>
        </div>
      </div>

      <div class="item" style="background-image:url('img-black\ \(2\).png');">
        <div class="contents">
          <div class="name">Necklace  </div>
          <div class="des">You have brains in your head. You have feet in your shoes</div>
          <button>See More</button>
        </div>
      </div>
    </div>

    <div class="button">
      <button class="prev">◁</button>
      <button class="next">▷</button>
    </div>
  </div>

<!-- footer -->

<footer >
  <div class="footer-container">

    <div class="footer-section">
      <h3 >Payment Methods</h3>
      <div class="payment-logos">
        <img src="https://cdn-icons-png.flaticon.com/512/196/196578.png" alt="Visa">
        <img src="https://cdn-icons-png.flaticon.com/512/196/196565.png" alt="MasterCard">
        <img src="https://cdn-icons-png.flaticon.com/512/196/196566.png" alt="PayPal">

      </div>
    </div>

    <div class="footer-section">
      <h3>Help & Info</h3>
      <ul>
        <li ><a href="#">FAQ</a></li>
        <li><a href="#">Shipping & Returns</a></li>
        <li><a href="#">Jewelry Care</a></li>
        <li><a href="#">Privacy Policy</a></li>
        <li><a href="#">Terms & Conditions</a></li>
      </ul>
    </div>

    <div class="footer-section">
      <h3 data-aos="fade-up">Explore</h3>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Collections</a></li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Stores</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>

    <div class="footer-section">
      <h3 >Stay Connected</h3>
      <div class="social-icons">
        <a href="#" ><i class="fab fa-facebook-f"></i></a>
        <a href="#" ><i class="fab fa-instagram"></i></a>
        <a href="#" ><i class="fab fa-youtube"></i></a>
      </div>
      <div class="newsletter">
        <p >Join our newsletter to receive updates on new jewelry collections and exclusive offers.</p>
        <input type="email" placeholder="Enter your email">
        <button type="submit">SEND</button>
      </div>
    </div>

  </div>
<hr>
  <div class="footer-bottom" >
    © 2025 DiamondAura Jewelry | Designed by Diana Qazizadah
  </div>
</footer>

  <script>
    const next = document.querySelector(".next");
    const prev = document.querySelector(".prev");

    next.addEventListener("click", () => {
      const items = document.querySelectorAll(".item");
      document.querySelector(".slide").appendChild(items[0]);
    });

    prev.addEventListener("click", () => {
      const items = document.querySelectorAll(".item");
      document.querySelector(".slide").prepend(items[items.length - 1]);
    });
  </script>

<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
<script>
  const menuToggle = document.getElementById('menu-toggle');
  const navList = document.getElementById('nav-list');

  menuToggle.addEventListener('click', () => {
    navList.classList.toggle('show');
  });
  const links = document.querySelectorAll('nav ul li a');
  links.forEach(link => {
    link.addEventListener('click', () => {
      links.forEach(l => l.classList.remove('active'));
      link.classList.add('active');
    });
  });

</script>

<script>
  const hamburger = document.getElementById("hamburger");
  const sidebar = document.getElementById("sidebar");
  const overlay = document.getElementById("overlay");
  hamburger.addEventListener("click", () => {
    sidebar.classList.toggle("active");
    overlay.classList.toggle("active");
  });

  overlay.addEventListener("click", () => {
    sidebar.classList.remove("active");
    overlay.classList.remove("active");
  });
</script>

<script>
  function openMenu() {
    document.getElementById('mobileMenu').classList.add('active');
  }

  function closeMenu() {
    document.getElementById('mobileMenu').classList.remove('active');
  }
</script>

<script>
  AOS.init();
</script>

</body>
</html>
