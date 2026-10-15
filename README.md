
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Aditya Singh - Computer Store</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f4f7fb;
      color: #172033;
    }

    header {
      background: #101827;
      color: white;
      padding: 20px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
    }

    header h2 {
      color: #42caff;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 18px;
    }

    .hero {
      background: linear-gradient(120deg, #101827, #164d78);
      color: white;
      padding: 80px 8%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 35px;
      flex-wrap: wrap;
    }

    .hero-content {
      flex: 1 1 280px;
    }

    .hero h1 {
      font-size: clamp(36px, 5vw, 58px);
      margin-bottom: 20px;
    }

    .hero h1 span {
      color: #42caff;
    }

    .hero p {
      line-height: 1.7;
      margin-bottom: 25px;
      color: #d5e4f3;
    }

    .hero img {
      width: 100%;
      max-width: 430px;
      border-radius: 15px;
    }

    .btn {
      display: inline-block;
      border: none;
      background: #168cff;
      color: white;
      padding: 13px 22px;
      border-radius: 7px;
      text-decoration: none;
      cursor: pointer;
      font-size: 15px;
    }

    .products {
      padding: 60px 8%;
      text-align: center;
    }

    .products h2 {
      font-size: 34px;
      margin-bottom: 30px;
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(
        auto-fit, minmax(220px, 1fr)
      );
      gap: 25px;
    }

    .product {
      background: white;
      padding: 18px;
      border-radius: 12px;
      box-shadow: 0 5px 20px #15243a12;
      transition: transform 0.25s;
    }

    .product:hover {
      transform: translateY(-6px);
    }

    .product img {
      width: 100%;
      height: 190px;
      object-fit: contain;
      margin-bottom: 15px;
    }

    .product h3 {
      margin-bottom: 10px;
    }

    .product p {
      color: #596579;
      margin-bottom: 15px;
      line-height: 1.5;
    }

    .price {
      font-size: 22px;
      color: #087b42;
      font-weight: bold;
      margin-bottom: 15px;
    }

    .about {
      background: #e4f2ff;
      text-align: center;
      padding: 45px 8%;
      line-height: 1.8;
    }

    footer {
      background: #101827;
      color: white;
      padding: 28px;
      text-align: center;
      line-height: 1.8;
    }

    @media (max-width: 600px) {
      header {
        padding: 20px 5%;
      }

      nav a {
        margin-left: 8px;
        font-size: 13px;
      }

      .hero {
        padding: 50px 6%;
      }

      .products {
        padding: 45px 6%;
      }
    }
  </style>
</head>

<body>

  <header>
    <h2>ADITYA COMPUTERS</h2>

    <nav>
      <a href="#home">Home</a>
      <a href="#products">Products</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <div class="hero-content">
      <h1>Upgrade Your <span>Technology</span></h1>

      <p>
        Discover powerful computers, laptops and gaming PCs.
        Find the right technology for work, study and gaming.
      </p>

      <a href="#products" class="btn">Explore Products</a>
    </div>

    <img
      src="https://images.unsplash.com/photo-1593640408182-31c70c8268f5?auto=format&fit=crop&w=900&q=85"
      alt="Desktop computer setup"
    >
  </section>

  <section class="products" id="products">
    <h2>Our Products</h2>

    <div class="product-grid">

      <div class="product">
        <img
          src="https://images.unsplash.com/photo-1496181133206-80ce9b88a853?auto=format&fit=crop&w=600&q=80"
          alt="Laptop"
        >
        <h3>Everyday Laptop</h3>
        <p>For study, office and daily use.</p>
        <div class="price">₹45,000</div>
        <button class="btn" onclick="buy('Everyday Laptop')">
          Buy Now
        </button>
      </div>

      <div class="product">
        <img
          src="https://images.unsplash.com/photo-1587202372775-e229f172b9d7?auto=format&fit=crop&w=600&q=80"
          alt="Gaming computer"
        >
        <h3>Gaming PC</h3>
        <p>For gaming and demanding tasks.</p>
        <div class="price">₹75,000</div>
        <button class="btn" onclick="buy('Gaming PC')">
          Buy Now
        </button>
      </div>

      <div class="product">
        <img
          src="https://images.unsplash.com/photo-1527443224154-c4a3942d3acf?auto=format&fit=crop&w=600&q=80"
          alt="Computer monitor"
        >
        <h3>Computer Monitor</h3>
        <p>A clear display for work and entertainment.</p>
        <div class="price">₹12,000</div>
        <button class="btn" onclick="buy('Computer Monitor')">
          Buy Now
        </button>
      </div>

    </div>
  </section>

  <section class="about">
    <h2>About Our Store</h2>
    <p>
      Welcome to Aditya Computers!
      Your demo destination for computers and technology.
    </p>
  </section>

  <footer id="contact">
    <h3>Aditya Computers</h3>
    <p>Website created by Aditya Singh</p>
    <p>Contact: your-email@example.com</p>
    <p>© 2026 Aditya Computers</p>
  </footer>

  <script>
    function buy(productName) {
      alert(
        "Thank you for your interest in " +
        productName +
        "! Online ordering is not enabled yet."
      );
    }
  </script>

</body>
</html>
