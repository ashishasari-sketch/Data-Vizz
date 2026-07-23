# Data-Vizz
Amit Kaps data visualisation 2026
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VelociKids - Ready for Big Adventures!</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Nunito:wght@400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- CSS RESET & VARIABLES --- */
        :root {
            --primary: #FF5E5B;       /* Fun Coral/Red */
            --secondary: #00CECB;     /* Bright Turquoise */
            --accent: #FFED66;        /* Sunny Yellow */
            --dark: #2E4057;          /* Deep Blue/Gray */
            --light: #F9F9FB;         /* Off-white */
            --white: #FFFFFF;
            --radius: 16px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Nunito', sans-serif;
            color: var(--dark);
            background-color: var(--light);
            line-height: 1.6;
        }

        h1, h2, h3, .logo {
            font-family: 'Fredoka', cursive;
        }

        /* --- CONTAINER --- */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- BUTTONS --- */
        .btn {
            display: inline-block;
            padding: 14px 28px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
        }

        .btn-primary {
            background-color: var(--primary);
            color: var(--white);
            box-shadow: 0 4px 14px rgba(255, 94, 91, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 94, 91, 0.6);
        }

        .btn-secondary {
            background-color: var(--secondary);
            color: var(--white);
        }

        .btn-secondary:hover {
            transform: translateY(-2px);
            opacity: 0.9;
        }

        /* --- HEADER / NAVBAR --- */
        header {
            background-color: var(--white);
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            color: var(--primary);
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 20px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* --- HERO SECTION --- */
        .hero {
            padding: 80px 0;
            background: linear-gradient(135deg, #FFF5F5 0%, #E6FAF9 100%);
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .hero-text h1 {
            font-size: 3.2rem;
            color: var(--dark);
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-text h1 span {
            color: var(--primary);
        }

        .hero-text p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: #556B82;
        }

        .hero-image img {
            width: 100%;
            border-radius: var(--radius);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        /* --- FEATURES SECTION --- */
        .features {
            padding: 80px 0;
            background-color: var(--white);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: var(--dark);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background-color: var(--light);
            padding: 30px;
            border-radius: var(--radius);
            text-align: center;
            transition: transform 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .feature-card h3 {
            font-size: 1.4rem;
            margin-bottom: 10px;
        }

        /* --- PRODUCTS SECTION --- */
        .products {
            padding: 80px 0;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: var(--white);
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            text-align: center;
            padding-bottom: 25px;
        }

        .product-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .product-card h3 {
            font-size: 1.5rem;
            margin: 15px 0 5px;
        }

        .product-card .age {
            color: var(--secondary);
            font-weight: 700;
            margin-bottom: 15px;
        }

        .product-card .price {
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 15px;
            color: var(--dark);
        }

        /* --- TESTIMONIALS --- */
        .testimonials {
            padding: 80px 0;
            background-color: var(--white);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background-color: var(--light);
            padding: 30px;
            border-radius: var(--radius);
            position: relative;
        }

        .testimonial-card p {
            font-style: italic;
            margin-bottom: 15px;
        }

        .testimonial-card h4 {
            color: var(--primary);
            font-weight: 700;
        }

        /* --- FOOTER / CTA --- */
        .cta-section {
            background: linear-gradient(135deg, var(--primary) 0%, #FF8A88 100%);
            color: var(--white);
            text-align: center;
            padding: 80px 20px;
        }

        .cta-section h2 {
            font-size: 2.8rem;
            margin-bottom: 15px;
        }

        .cta-section p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .btn-cta {
            background-color: var(--accent);
            color: var(--dark);
            font-size: 1.2rem;
        }

        .btn-cta:hover {
            background-color: #FFF085;
            transform: translateY(-2px);
        }

        footer {
            background-color: var(--dark);
            color: var(--white);
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
        }

        /* --- RESPONSIVE DESIGN --- */
        @media (max-width: 768px) {
            .hero-grid {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-text h1 {
                font-size: 2.4rem;
            }

            .nav-links {
                display: none; /* Can be enhanced with a JS toggle menu */
            }
        }
    </style>
</head>
<body>

    <!-- NAVBAR -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Veloci<span>Kids</span></a>
                <ul class="nav-links">
                    <li><a href="#features">Why Us</a></li>
                    <li><a href="#products">Bikes</a></li>
                    <li><a href="#reviews">Reviews</a></li>
                </ul>
                <a href="#products" class="btn btn-primary">Shop Now</a>
            </nav>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="container">
            <div class="hero-grid">
                <div class="hero-text">
                    <h1>Built for Big Smiles & <span>Fearless Adventures</span></h1>
                    <p>Ultra-lightweight, super durable, and designed specifically for small riders. Give your child the confidence to ride further.</p>
                    <a href="#products" class="btn btn-primary">Find the Perfect Bike</a>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1517649763962-0c623266010b?auto=format&fit=crop&w=800&q=80" alt="Happy child riding a bicycle">
                </div>
            </div>
        </div>
    </section>

    <!-- FEATURES SECTION -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">Designed for Kids, Approved by Parents</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🪶</div>
                    <h3>Featherlight Frame</h3>
                    <p>Up to 40% lighter than standard kids' bikes, making balancing and pedaling effortlessly easy.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🛡️</div>
                    <h3>Safety First</h3>
                    <p>Child-sized hand brakes, non-toxic finishes, and enclosed chains to keep tiny fingers safe.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌱</div>
                    <h3>Grows With Them</h3>
                    <p>Fully adjustable seats and handlebars ensure the bike lasts through multiple growth spurts.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- PRODUCTS SECTION -->
    <section class="products" id="products">
        <div class="container">
            <h2 class="section-title">Choose Their Next Ride</h2>
            <div class="product-grid">
                <!-- Product 1 -->
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1507035895480-2b3156c31fc8?auto=format&fit=crop&w=600&q=80" alt="Balance Bike">
                    <h3>The Sprout</h3>
                    <div class="age">Ages 1.5 - 3.5 Years</div>
                    <div class="price">$129</div>
                    <a href="#" class="btn btn-secondary">Learn More</a>
                </div>
                <!-- Product 2 -->
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1485965120184-e220f721d03e?auto=format&fit=crop&w=600&q=80" alt="First Pedal Bike">
                    <h3>The Cruiser Jr.</h3>
                    <div class="age">Ages 3 - 6 Years</div>
                    <div class="price">$219</div>
                    <a href="#" class="btn btn-secondary">Learn More</a>
                </div>
                <!-- Product 3 -->
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1532298229144-0ec0c57515c7?auto=format&fit=crop&w=600&q=80" alt="All-Terrain Bike">
                    <h3>The TrailBlazer</h3>
                    <div class="age">Ages 6 - 10 Years</div>
                    <div class="price">$299</div>
                    <a href="#" class="btn btn-secondary">Learn More</a>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS SECTION -->
    <section class="testimonials" id="reviews">
        <div class="container">
            <h2 class="section-title">What Parents Are Saying</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p>"My 4-year-old learned to ride without training wheels in just two days on The Cruiser Jr. Lightweight design made all the difference!"</p>
                    <h4>— Sarah M.</h4>
                </div>
                <div class="testimonial-card">
                    <p>"Extremely well-built and safe. You can tell real thought went into the sizing of the brake levers for small hands."</p>
                    <h4>— David K.</h4>
                </div>
                <div class="testimonial-card">
                    <p>"Worth every penny. It's so light that my daughter can pick it up herself when it drops. Highly recommended!"</p>
                    <h4>— Jessica T.</h4>
                </div>
            </div>
        </div>
    </section>

    <!-- CALL TO ACTION -->
    <section class="cta-section">
        <div class="container">
            <h2>Ready to Start the Journey?</h2>
            <p>Free shipping on all orders + 30-day risk-free trial.</p>
            <a href="#products" class="btn btn-cta">Get Your Bike Today</a>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <p>&copy; 2026 VelociKids Bicycles Inc. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>