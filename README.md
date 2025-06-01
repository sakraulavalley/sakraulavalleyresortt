<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Sakraula Valley Resort & Restaurant</title>
  <!-- Tailwind CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <!-- Swiper.js CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" rel="stylesheet">
  <style>
    /* Custom Styles */
    .hero-section {
      background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1566073771259-6a8506099945?q=80&w=2070&auto=format&fit=crop');
      background-size: cover;
      background-position: center;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-align: center;
    }
    .booking-form {
      background: rgba(255, 255, 255, 0.95);
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
    }
    .swiper-slide img {
      width: 100%;
      height: 400px;
      object-fit: cover;
      border-radius: 10px;
    }
    .navbar {
      transition: background-color 0.3s;
    }
    .navbar.scrolled {
      background-color: rgba(0, 0, 0, 0.8);
    }
  </style>
</head>
<body class="font-sans">
  <!-- Navigation Bar -->
  <nav class="navbar fixed top-0 w-full bg-transparent z-50 py-4">
    <div class="container mx-auto flex justify-between items-center px-4">
      <a href="#" class="text-2xl font-bold text-white">The Sakraula Valley Resort</a>
      <ul class="flex space-x-6 text-white">
        <li><a href="#home" class="hover:text-yellow-400 transition">Home</a></li>
        <li><a href="#booking" class="hover:text-yellow-400 transition">Book Now</a></li>
        <li><a href="#gallery" class="hover:text-yellow-400 transition">Gallery</a></li>
        <li><a href="#about" class="hover:text-yellow-400 transition">About</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="hero-section">
    <div>
      <h1 class="text-5xl font-bold mb-4">Welcome to The Sakraula Valley Resort & Restaurant</h1>
      <p class="text-xl mb-6">Experience serenity and luxury amidst nature. Enjoy breathtaking views, exquisite dining, and unparalleled hospitality.</p>
      <a href="#booking" class="bg-yellow-500 text-white px-6 py-3 rounded-full hover:bg-yellow-600 transition">Book Now</a>
    </div>
  </section>

  <!-- Booking Form -->
  <section id="booking" class="py-16 bg-gray-100">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8">Book Your Stay</h2>
      <div class="booking-form max-w-lg mx-auto">
        <form id="bookingForm" onsubmit="handleBooking(event)">
          <div class="mb-4">
            <label class="block text-gray-700 mb-2" for="name">Name</label>
            <input type="text" id="name" class="w-full p-2 border rounded" required>
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 mb-2" for="email">Email</label>
            <input type="email" id="email" class="w-full p-2 border rounded" required>
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 mb-2" for="checkin">Check-in Date</label>
            <input type="date" id="checkin" class="w-full p-2 border rounded" required>
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 mb-2" for="checkout">Check-out Date</label>
            <input type="date" id="checkout" class="w-full p-2 border rounded" required>
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 mb-2" for="guests">Number of Guests</label>
            <input type="number" id="guests" min="1" class="w-full p-2 border rounded" required>
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 mb-2" for="room">Room Type</label>
            <select id="room" class="w-full p-2 border rounded" required>
              <option value="">Select Room Type</option>
              <option value="standard">Standard Room</option>
              <option value="deluxe">Deluxe Room</option>
              <option value="suite">Luxury Suite</option>
            </select>
          </div>
          <button type="submit" class="w-full bg-yellow-500 text-white p-3 rounded hover:bg-yellow-600 transition">Submit Booking</button>
        </form>
      </div>
    </div>
  </section>

  <!-- Picture Slider -->
  <section id="gallery" class="py-16">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8">Our Resort Gallery</h2>
      <div class="swiper mySwiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?q=80&w=2070&auto=format&fit=crop" alt="Resort Room">
          </div>
          <div class="swiper-slide">
            <img src="https://images.unsplash.com/photo-1578683014728-c73504ce5477?q=80&w=2070&auto=format&fit=crop" alt="Resort Pool">
          </div>
          <div class="swiper-slide">
            <img src="https://images.unsplash.com/photo-1445019980597-93fa8acb246c?q=80&w=2070&auto=format&fit=crop" alt="Resort Lobby">
          </div>
        </div>
        <div class="swiper-button-next"></div>
        <div class="swiper-button-prev"></div>
        <div class="swiper-pagination"></div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-16 bg-gray-100">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8">About The Sakraula Valley Resort & Restaurant</h2>
      <div class="max-w-3xl mx-auto text-center">
        <p class="text-lg mb-4">Nestled in the heart of nature, The Sakraula Valley Resort & Restaurant offers a perfect blend of luxury and tranquility. Our resort features spacious rooms, a rooftop restaurant, and stunning natural surroundings to make your stay unforgettable.</p>
        <p class="text-lg mb-4">Contact us:</p>
        <p class="text-lg mb-2"><strong>Email:</strong> <a href="mailto:sakraulavalley@gmail.com" class="text-yellow-500 hover:underline">sakraulavalley@gmail.com</a></p>
        <p class="text-lg mb-4"><strong>Mobile:</strong> <a href="tel:+919557958581" class="text-yellow-500 hover:underline">+91 9557958581</a></p>
        <a href="#booking" class="bg-yellow-500 text-white px-6 py-3 rounded-full hover:bg-yellow-600 transition">Book Your Stay</a>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white py-8">
    <div class="container mx-auto px-4 text-center">
      <p>© 2025 The Sakraula Valley Resort & Restaurant. All rights reserved.</p>
    </div>
  </footer>

  <!-- Swiper.js CDN -->
  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
  <script>
    // Initialize Swiper
    const swiper = new Swiper('.mySwiper', {
      loop: true,
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      autoplay: {
        delay: 3000,
      },
    });

    // Navbar Scroll Effect
    window.addEventListener('scroll', () => {
      const navbar = document.querySelector('.navbar');
      if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
      } else {
        navbar.classList.remove('scrolled');
      }
    });

    // Booking Form Handler
    function handleBooking(event) {
      event.preventDefault();
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const checkin = document.getElementById('checkin').value;
      const checkout = document.getElementById('checkout').value;
      const guests = document.getElementById('guests').value;
      const room = document.getElementById('room').value;

      if (name && email && checkin && checkout && guests && room) {
        const subject = encodeURIComponent(`New Booking from ${name}`);
        const body = encodeURIComponent(
          `Booking Details:\nName: ${name}\nEmail: ${email}\nCheck-in: ${checkin}\nCheck-out: ${checkout}\nGuests: ${guests}\nRoom Type: ${room}`
        );
        window.location.href = `mailto:sakraulavalley@gmail.com?subject=${subject}&body=${body}`;
        alert('Booking submitted! You are being redirected to your email client.');
        document.getElementById('bookingForm').reset();
      } else {
        alert('Please fill out all fields.');
      }
    }
  </script>
</body>
</html># sakraulavalleyresortt
