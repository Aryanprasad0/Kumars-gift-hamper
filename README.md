<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Kumars Gift Hamper - Gifts</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #fafafa;
    }
    header {
      background: #7d5fff;
      color: #fff;
      padding: 1em 0;
      text-align: center;
    }
    nav a {
      color: #fff;
      margin: 0 1em;
      text-decoration: none;
    }
    main {
      padding: 2em;
    }
    .product-list {
      display: flex;
      gap: 2em;
      flex-wrap: wrap;
      justify-content: center;
    }
    .product {
      background: #fff;
      border: 1px solid #eee;
      border-radius: 8px;
      padding: 1em;
      text-align: center;
      width: 220px;
      box-shadow: 0 2px 8px #eee;
    }
    .product img {
      width: 200px;
      height: 200px;
      object-fit: cover;
      margin-bottom: 1em;
    }
    .price {
      display: block;
      margin-top: 0.5em;
      font-weight: bold;
      color: #7d5fff;
    }
    .contact-form {
      max-width: 400px;
      margin: 2em auto;
      display: flex;
      flex-direction: column;
      gap: 1em;
      background: #fff;
      padding: 1.5em;
      border-radius: 8px;
      box-shadow: 0 2px 8px #eee;
    }
    .contact-form label {
      font-weight: bold;
    }
    .contact-form input,
    .contact-form textarea {
      padding: 0.5em;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .contact-form button {
      background: #7d5fff;
      color: #fff;
      border: none;
      padding: 0.7em;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1em;
    }
    .tabs {
      display: flex;
      justify-content: center;
      margin-bottom: 2em;
      gap: 2em;
    }
    .tablink {
      padding: 0.5em 1.5em;
      background: #eee;
      border: none;
      border-radius: 4px 4px 0 0;
      cursor: pointer;
      font-size: 1em;
      color: #333;
    }
    .tablink.active {
      background: #7d5fff;
      color: #fff;
      font-weight: bold;
    }
    footer {
      background: #222;
      color: #fff;
      text-align: center;
      padding: 1em 0;
      margin-top: 2em;
    }
  </style>
</head>
<body>
  <header>
    <h1>Kumars Gift Hamper</h1>
    <nav>
      <span>Online Store</span>
    </nav>
  </header>

  <div class="tabs">
    <button class="tablink active" onclick="showTab('products')">Gifts</button>
    <button class="tablink" onclick="showTab('contact')">Contact</button>
  </div>

  <main>
    <section id="products">
      <h2>Our Gifts</h2>
      <div class="product-list">
        <div class="product">
          <img src="https://via.placeholder.com/200" alt="Gift Hamper 1">
          <h3>Classic Gift Hamper</h3>
          <p>Perfect for any occasion. Includes chocolates, snacks, and more!</p>
          <span class="price">₹999</span>
        </div>
        <div class="product">
          <img src="https://via.placeholder.com/200" alt="Gift Hamper 2">
          <h3>Festive Gift Basket</h3>
          <p>Celebrate with a selection of festive treats and goodies.</p>
          <span class="price">₹1299</span>
        </div>
        <div class="product">
          <img src="https://via.placeholder.com/200" alt="Gift Hamper 3">
          <h3>Premium Gift Box</h3>
          <p>Luxury items for that special someone in your life.</p>
          <span class="price">₹1999</span>
        </div>
      </div>
    </section>

    <section id="contact" style="display:none;">
      <h2>Contact Us</h2>
      <form class="contact-form" action="mailto:your-email@example.com" method="post" enctype="text/plain">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        
        <label for="message">Message:</label>
        <textarea id="message" name="message" rows="5" required></textarea>
        
        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Kumars Gift Hamper</p>
  </footer>
  <script>
    function showTab(tab) {
      document.getElementById('products').style.display = tab === 'products' ? '' : 'none';
      document.getElementById('contact').style.display = tab === 'contact' ? '' : 'none';
      const tablinks = document.querySelectorAll('.tablink');
      tablinks.forEach((btn, idx) => {
        if ((tab === 'products' && idx === 0) || (tab === 'contact' && idx === 1)) {
          btn.classList.add('active');
        } else {
          btn.classList.remove('active');
        }
      });
    }
  </script>
</body>
</html>