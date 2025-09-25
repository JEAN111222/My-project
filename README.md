<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TrendyFits Clothing</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f9f9f9;
      color: #333;
    }
    header {
      background: #222;
      color: #fff;
      padding: 15px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    header h1 { margin: 0; font-size: 24px; cursor: pointer; }
    nav { display: flex; gap: 20px; align-items: center; }
    nav a { color: #fff; text-decoration: none; font-weight: bold; cursor: pointer; }
    nav a:hover { text-decoration: underline; }
    section { display: none; padding: 40px 20px; }
    section.active { display: block; }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
    }
/* Shop Page Images - pantay lahat pero kita buong image */
    #shop .product img,
    #shop .category img {
      width: 100%;
      height: 250px;       /* fixed height */
      object-fit: contain; /* buo ang image */
      background: #fff;
      border-radius: 6px;
    }

    /* Desktop adjustment */
    @media (min-width: 1024px) {
      #shop .product img,
      #shop .category img {
        height: 300px;
      }
    }

    @media (min-width: 1024px) {
      #shop .product img { height: 300px; }
    }
    #shop .product {
      background: #fff;
      padding: 15px;
      border-radius: 8px;
      text-align: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 380px;
    }
    #shop .product h3 {
      font-size: 16px;
      font-weight: bold;
      margin: 10px 0 5px;
      height: 40px;
      overflow: hidden;
    }
    #shop .product p { font-size: 15px; margin: 5px 0 10px; color: #444; }
    #shop .product button {
      padding: 10px 15px;
      background: #222;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .cart, #payment-section, #receipt {
      padding: 20px;
      background: #fff;
      margin-top: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .cart table, #receipt table {
      width: 100%;
      border-collapse: collapse;
    }
    .cart th, .cart td, #receipt th, #receipt td {
      padding: 10px;
      border: 1px solid #ddd;
      text-align: center;
    }
    .qty-btn {
      background: #222;
      color: #fff;
      border: none;
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
    }
    .delete-btn {
      background: red;
      color: #fff;
      border: none;
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
    }
    #payment-section, #receipt { display: none; }
    footer {
      background: #222;
      color: #fff;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
    .homepage-section {
      text-align: center;
      padding: 20px;
    }
    .landscape-image {
      position: relative;
      width: 100%;
      max-width: 1200px;
      margin: auto;
    }
    .landscape-image img {
      width: 100%;
      height: 400px;
      object-fit: cover;
      display: block;
    }
    
.overlay-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  background: rgba(255, 255, 255, 0.85); /* white background na semi-transparent */
  padding: 15px 25px; /* sakto lang laki */
  border-radius: 6px;
  max-width: 80%; /* hindi lalagpas sa image width */
}

.overlay-text h2 {
  margin: 0;
  font-size: 22px; /* sakto lang font size */
  color: #222;
}

.overlay-text p {
  margin: 8px 0 0;
  font-size: 16px;
  color: #444;
}



    .section-title {
      margin: 30px 0 20px;
      font-size: 28px;
      font-weight: bold;
      color: #333;
    }
    .image-row {
      display: flex;
      gap: 20px;
      justify-content: center;
      max-width: 1200px;
      margin: auto;
    }
    .image-card {
      width: 300px;
    }
    .image-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 8px;
    }
    .image-label {
      margin-top: 10px;
      font-weight: bold;
      font-size: 18px;
      color: #444;
    }
    
  </style>
</head>
<body>

<header>
  <h1 onclick="showSection('home')">TrendyFits Clothing</h1>
  <nav>
    <a onclick="showSection('home')">Home</a>
    <a onclick="showSection('about')">About Us</a>
    <a onclick="showSection('shop')">Shop</a>
    <a onclick="showSection('lookbook')">Lookbook</a>
    <a onclick="showSection('contact')">Contact Us</a>
  </nav>
</header>
<!-- Home -->
  <section id="home" class="active">
    <div class="homepage-section">
      <div class="landscape-image">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images%20(3).jpeg" alt="Main Banner">
       <div class="overlay-text">
  <h2>Clothing Business Website</h2>
  <p>Be bold. Be stylish. Be you</p>
</div>


      </div>
      <h2 class="section-title">CATEGORIES</h2>
      <div class="image-row">
        <div class="image-card">
          <img src="https://uploads.onecompiler.io/4395x8y2x/43xhrpayh/Messenger_creation_FC0C106D-785D-4789-80B2-9A692FB0EED0.jpeg" alt="Men's Wear">
          <div class="image-label">Dress</div>
        </div>
        <div class="image-card">
          <img src="https://uploads.onecompiler.io/4395x8y2x/43xhrpayh/Messenger_creation_0B1216F3-0C01-47FF-B49A-C2B9F345C845.jpeg" alt="Women's Wear">
          <div class="image-label">Pants</div>
        </div>
        <div class="image-card">
          <img src="https://uploads.onecompiler.io/4395x8y2x/43xhrpayh/Messenger_creation_BEAA847C-02C5-4DA5-B7C5-2DD9BF11EF92.jpeg" alt="Accessories">
          <div class="image-label">T-shirt</div>
        </div>
    </div>
  </section>




  <!-- Shop -->
  <section id="shop">
    <h2>Shop by Category</h2>
    <div class="category-grid">
      <div class="category" onclick="filterCategory('men')">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images%20(1).jpeg" alt="Men's Wear">
        <h3>Men's Wear</h3>
      </div>
      <div class="category" onclick="filterCategory('women')">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/Mental-Strong-Women-min.jpg" alt="Women's Wear">
        <h3>Women's Wear</h3>
      </div>
<div class="category" onclick="filterCategory('baby')">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/images%20(4).jpeg" alt="Women's Wear">
        <h3>Baby clothes</h3>
      </div>
      
      <div class="category" onclick="filterCategory('all')">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images%20(2).jpeg" alt="All Products">
        <h3>All Products</h3>
      </div>
    </div>

    <h2 style="margin-top:40px;">Featured Products</h2>
    <div class="product-grid" id="product-list">
      <div class="product" data-category="men">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfgnssz/CNKN-2000080925005_1.jpg" alt="Jacket">
        <h3>Stylish Jacket</h3>
        <p>₱1200</p>
        <button onclick="addToCart('Stylish Jacket',1200)">Add to Cart</button>
      </div>
      <div class="product" data-category="men">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfgnssz/CNKN-2000080929005_1.jpg" alt="Shirt">
        <h3>Casual Shirt</h3>
        <p>₱800</p>
        <button onclick="addToCart('Casual Shirt',800)">Add to Cart</button>
      </div>
      <div class="product" data-category="women">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/trendyol-9739-7132463-1.webp" alt="Dress">
        <h3>Elegant Dress</h3>
        <p>₱1500</p>
        <button onclick="addToCart('Elegant Dress',1500)">Add to Cart</button>
      </div>
      <div class="product" data-category="women">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/-473Wx593H-701543483-grey-MODEL.jpg" alt="T-shirt">
        <h3>Women Oversized Fit Cotton Graphic T-shirt</h3>
        <p>₱100</p>
        <button onclick="addToCart('Women Oversized Fit Cotton Graphic T-shirt',100)">Add to Cart</button>
      </div>
      <div class="product" data-category="women">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images.jpeg" alt="Pants">
        <h3>Ladies Pants & Trousers</h3>
        <p>₱100</p>
        <button onclick="addToCart('Ladies Pants & Trousers',100)">Add to Cart</button>
      </div>
 <div class="product" data-category="baby">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_CBE2FB12-C26F-4B7E-A913-E507639650F3.jpeg" alt="Pants">
        
        <p>₱400</p>
        <button onclick="addToCart('Ladies Pants & Trousers',400)">Add to Cart</button>
      </div>
 <div class="product" data-category="baby">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_63897A39-16C8-4315-B57D-8D7D32C7869E.jpeg" alt="Pants">
        
        <p>₱300</p>
        <button onclick="addToCart('Ladies Pants & Trousers',300)">Add to Cart</button>
      </div>
      
 <div class="product" data-category="baby">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_B29EBDAF-9C0E-4AC3-A14B-6F85BA426C57.jpeg" alt="Pants">
        
        <p>₱600</p>
        <button onclick="addToCart('Ladies Pants & Trousers',600)">Add to Cart</button>
      </div>
      
 <div class="product" data-category="baby">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_B155C690-A800-47C1-B8FD-806772694CD6.jpeg" alt="Pants">
        
        <p>₱200</p>
        <button onclick="addToCart('Ladies Pants & Trousers',200)">Add to Cart</button>
      </div>
      
      
    </div>
    


  <!-- Cart -->
  <div class="cart" id="cart-section">
    <h3>Your Cart</h3>
    <table id="cart-table">
      <thead>
        <tr>
          <th>Product</th><th>Price</th><th>Qty</th><th>Subtotal</th><th>Action</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <h3>Total: ₱<span id="total">0</span></h3>
    <button onclick="showPayment()">Proceed to Checkout</button>
  </div>

  <!-- Payment -->
  <div id="payment-section">
    <h3>Select Payment Method:</h3>
    <label><input type="radio" name="payment" value="GCash"> GCash</label><br>
    <label><input type="radio" name="payment" value="PayPal"> PayPal</label><br>
    <label><input type="radio" name="payment" value="Cash on Delivery"> Cash on Delivery</label><br><br>
    <button onclick="checkout()">Confirm Payment</button>
  </div>

  <!-- Receipt -->
  <div id="receipt">
    <h3>🧾 Receipt / Resibo</h3>
    <div id="receipt-details"></div>
  </div>
</section>

<!-- About -->
<section id="about" style="
  background: url('https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images%20(3).jpeg') no-repeat center center;
  background-size: cover;
  background-attachment: fixed;
  padding: 60px 20px;
  text-align: center;
  color: #333;
">
  <div style="
    background: rgba(255, 255, 255, 0.92);
    width: 90%;
    max-width: 900px;
    margin: auto;
    padding: 30px 20px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
  ">
    <h2>About Us</h2>
    <p style="font-size: 18px; line-height: 1.6;">
      At <strong>TrendyFits Clothing</strong>, we believe fashion is all about expressing yourself with confidence. 
      That’s why we offer trendy, comfortable, and affordable outfits that match the lifestyle of today’s young men and women. 
      From casual wear to stylish fits, our goal is to make fashion simple, fun, and accessible to everyone.
    </p>
    <p style="font-size: 18px; line-height: 1.6;">
      Our website is designed to give you an easy and enjoyable shopping experience. 
      You can explore the latest collections, check product details, and place your orders anytime, anywhere. 
      With TrendyFits, fashion meets convenience—helping you look good and feel good every day.
    </p>
  </div>
</section>


<!-- Lookbook -->
<section id="lookbook" style="
  background: url('https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images%20(3).jpeg') no-repeat center center/cover;
  padding: 60px 20px;
  text-align: center;
">
  <div style="
    background: rgba(255, 255, 255, 0.9);
    max-width: 1100px;
    margin: auto;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
  ">
    <h2>Lookbook</h2>
    <p>Explore our latest collections and fashion inspirations below:</p>

    <!-- Image gallery -->
    <div style="
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 30px;
    ">
      <!-- Item 1 -->
      <div style="
        background: #fff; 
        border-radius: 10px; 
        overflow: hidden; 
        box-shadow: 0 4px 8px rgba(0,0,0,0.1); 
        display: flex; 
        flex-direction: column; 
        height: 100%;
      ">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_BE699A24-D105-492A-86F5-F4B5865F73B7.jpeg" alt="Look 1" style="width:100%; height:250px; object-fit:cover;">
        <div style="padding: 15px; flex-grow: 1;">
          <p><strong>Seasonal Collections – Example: Summer Vibes (shorts + crop tops), Cozy Fits (sweaters + jeans).</strong><br>Perfect for everyday comfort.</p>
        </div>
      </div>

      <!-- Item 2 -->
      <div style="
        background: #fff; 
        border-radius: 10px; 
        overflow: hidden; 
        box-shadow: 0 4px 8px rgba(0,0,0,0.1); 
        display: flex; 
        flex-direction: column; 
        height: 100%;
      ">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_C7C5F323-918A-4B6C-96BD-898FD89D5520.jpeg" alt="Look 2" style="width:100%; height:250px; object-fit:cover;">
        <div style="padding: 15px; flex-grow: 1;">
          <p><strong></strong>Trendy Styles – Streetwear, Casual Chic, Minimalist, Date Night Outfit, etc.<br>Stylish and timeless pieces.</p>
        </div>
      </div>

      <!-- Item 3 -->
      <div style="
        background: #fff; 
        border-radius: 10px; 
        overflow: hidden; 
        box-shadow: 0 4px 8px rgba(0,0,0,0.1); 
        display: flex; 
        flex-direction: column; 
        height: 100%;
      ">
        <img src="https://uploads.onecompiler.io/4395x8y2x/43xjrxf97/Messenger_creation_857F2F6B-2B8E-47F8-91F4-AAE26E80560F.jpeg" alt="Look 3" style="width:100%; height:250px; object-fit:cover;">
        <div style="padding: 15px; flex-grow: 1;">
          <p><strong>Mix & Match Ideas – Show how to pair tops with skirts, jeans, or accessories.</strong><br>Fresh looks for today’s vibe.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Contact -->
<section id="contact" style="
  background: url('https://uploads.onecompiler.io/4395x8y2x/43xfk3pf4/images%20(3).jpeg') no-repeat center center/cover;
  padding: 60px 20px;
  text-align: center;
">
  <div style="
    background: rgba(255, 255, 255, 0.95);
    max-width: 700px;
    margin: auto;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
  ">
    <h2>Contact Us</h2>
    <p>If you have any questions or inquiries, feel free to send us a message.</p>

    <!-- Contact Form -->
    <form id="contactForm" style="display: flex; flex-direction: column; gap: 15px; margin-top: 20px;">
      <input type="text" placeholder="Your Name" required 
        style="padding: 12px; border: 1px solid #ccc; border-radius: 5px; font-size: 16px;">

      <input type="email" placeholder="Your Email" required 
        style="padding: 12px; border: 1px solid #ccc; border-radius: 5px; font-size: 16px;">

      <textarea placeholder="Your Message" required rows="5"
        style="padding: 12px; border: 1px solid #ccc; border-radius: 5px; font-size: 16px; resize: none;"></textarea>

      <button type="submit" style="
        padding: 14px;
        background: #000;
        color: #fff;
        border: none;
        border-radius: 5px;
        font-size: 16px;
        cursor: pointer;
        transition: background 0.3s;
      ">Send Message</button>
    </form>

    <!-- Success Message -->
    <p id="successMessage" style="display:none; margin-top:20px; color:green; font-weight:bold;">
      ✅ Successfully Sent! Thank you for your message.
    </p>
  </div>
</section>

<script>
  // JavaScript to show success message
  document.getElementById("contactForm").addEventListener("submit", function(event){
    event.preventDefault(); // stop actual form submission
    document.getElementById("successMessage").style.display = "block";
    this.reset(); // clear form after sending
  });
</script>








<footer>
  <p>&copy; 2025 TrendyFits Clothing. All Rights Reserved.</p>
</footer>

<script>function showSection(id) {
      document.querySelectorAll("section").forEach(sec => sec.classList.remove("active"));
      document.getElementById(id).classList.add("active");
      window.scrollTo({ top: 0, behavior: "smooth" });
    }
    function filterCategory(category) {
      document.querySelectorAll("#product-list .product").forEach(product => {
        if (category === "all" || product.dataset.category === category) {
          product.style.display = "block";
        } else {
          product.style.display = "none";
        }
      });
    }

  

  let cart = [];
  function addToCart(product, price) {
    const found = cart.find(item => item.product === product);
    if (found) { found.qty++; }
    else { cart.push({ product, price, qty: 1 }); }
    renderCart();
  }
  function changeQty(index, amount) {
    cart[index].qty += amount;
    if (cart[index].qty <= 0) { cart.splice(index, 1); }
    renderCart();
  }
  function deleteItem(index) { cart.splice(index, 1); renderCart(); }
  function renderCart() {
    const tbody = document.querySelector("#cart-table tbody");
    tbody.innerHTML = "";
    let total = 0;
    cart.forEach((item, index) => {
      let subtotal = item.price * item.qty;
      total += subtotal;
      tbody.innerHTML += `
        <tr>
          <td>${item.product}</td>
          <td>₱${item.price}</td>
          <td>
            <button class="qty-btn" onclick="changeQty(${index},-1)">-</button>
            ${item.qty}
            <button class="qty-btn" onclick="changeQty(${index},1)">+</button>
          </td>
          <td>₱${subtotal}</td>
          <td><button class="delete-btn" onclick="deleteItem(${index})">Delete</button></td>
        </tr>`;
    });
    document.getElementById("total").innerText = total;
  }
  function showPayment() {
    if (cart.length === 0) { alert("Your cart is empty!"); return; }
    document.getElementById("payment-section").style.display = "block";
    document.getElementById("receipt").style.display = "none";
    document.getElementById("payment-section").scrollIntoView({ behavior: "smooth" });
  }
  function checkout() {
    if (cart.length === 0) { alert("Your cart is empty!"); return; }
    const paymentMethod = document.querySelector('input[name="payment"]:checked');
    if (!paymentMethod) { alert("Please select a payment method!"); return; }

    let receiptHTML = `
      <table>
        <thead>
          <tr><th>Product</th><th>Qty</th><th>Subtotal</th></tr>
        </thead>
        <tbody>`;
    let total = 0;
    cart.forEach(item => {
      let subtotal = item.price * item.qty;
      total += subtotal;
      receiptHTML += `<tr>
        <td>${item.product}</td>
        <td>${item.qty}</td>
        <td>₱${subtotal}</td>
      </tr>`;
    });
    receiptHTML += `</tbody></table>
      <p><strong>Total:</strong> ₱${total}</p>
      <p><strong>Payment Method:</strong> ${paymentMethod.value}</p>
      <p>✅ Thank you for shopping at TrendyFits Clothing!</p>`;

    document.getElementById("receipt-details").innerHTML = receiptHTML;
    document.getElementById("payment-section").style.display = "none";
    document.getElementById("receipt").style.display = "block";
    document.getElementById("receipt").scrollIntoView({ behavior: "smooth" });

    cart = [];
    renderCart();
  }
</script>

</body>
</html>


