<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Sales Mobil - Andi Irfan Maulana</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: 'Russo One', sans-serif;
            margin: 0;
            padding: 0;
            background: #f9f9f9;
            color: #333;
            scroll-behavior: smooth;
        }

        header {
            background: url('foto4.png') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 150px 20px;
            background-color: rgba(0, 0, 0, 0.7);
        }

        header h1 {
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        header p {
            font-size: 1.5em;
            font-weight: 300;
        }

        nav {
            background-color: #333;
            color: white;
            padding: 15px 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-size: 1.2em;
        }

        nav a:hover {
            text-decoration: underline;
        }

        .container {
            max-width: 1200px;
            margin: 50px auto;
            padding: 0 20px;
        }

        .about {
            display: flex;
            gap: 30px;
            align-items: center;
            margin-bottom: 60px;
        }

        .about img {
            border-radius: 10px;
            width: 100%;
            max-width: 500px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .about div {
            flex: 1;
        }

        .about h2 {
            font-size: 2.5em;
            color: #007bff;
            margin-bottom: 20px;
        }

        .about p {
            font-size: 1.2em;
            line-height: 1.6;
            color: #666;
        }

        .services {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .service {
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s, box-shadow 0.3s;
            color: white;
            position: relative;
            background-size: cover;
            background-position: center;
            height: 300px; /* Adjust height as needed */
        }

        .consult {
            background-image: url('sales2.jpg');
        }

        .offer {
            background-image: url('penawaran.jpg');
        }

        .test-drive {
            background-image: url('tes.jpg');
        }

        .service h3 {
            font-size: 2em;
            color: #fff;
            margin-bottom: 15px;
        }

        .service p {
            font-size: 1.2em;
            color: #ddd;
        }

        .service:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .gallery {
            display: flex;
            overflow-x: auto;
            gap: 15px;
            padding: 20px 0;
            scroll-snap-type: x mandatory;
        }

        .gallery img {
            flex: 0 0 auto;
            width: 200px;
            height: 150px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            scroll-snap-align: start;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .testimonials {
            margin-bottom: 60px;
        }

        .testimonial {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            margin-bottom: 20px;
            display: flex;
            justify-content: center;
        }

        .testimonial img {
            height: 60px;
            margin: 0 10px;
        }

        .contact {
            background: white;
            padding: 60px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            text-align: center;
            margin-bottom: 60px;
        }

        .contact h2 {
            font-size: 2.5em;
            color: #007bff;
            margin-bottom: 20px;
        }

        .contact p {
            font-size: 1.2em;
            color: #666;
            margin-bottom: 30px;
        }

        .contact .social {
            margin-bottom: 20px;
        }

        .contact .social a {
            display: inline-block;
            margin: 0 10px;
            transition: transform 0.3s;
        }

        .contact .social img {
            height: 40px;
            transition: opacity 0.3s;
        }

        .contact .social img:hover {
            opacity: 0.8;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
        }

        footer p {
            margin: 0;
        }

        .map {
            width: 100%;
            height: 400px;
            border: 0;
            border-radius: 10px;
            margin-bottom: 60px;
        }

        /* Gallery Modal Styles */
        .gallery-item {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .gallery-item img {
            max-width: 90%;
            max-height: 80%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
        }

        .gallery-item .caption {
            color: #fff;
            margin-top: 20px;
            font-size: 1.2em;
            text-align: center;
        }

        .gallery-item .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 2em;
            color: #fff;
            cursor: pointer;
        }

        /* Media Queries for Mobile Devices */
        @media (max-width: 768px) {
            header {
                padding: 100px 20px;
            }

            header h1 {
                font-size: 2.5em;
            }

            header p {
                font-size: 1.2em;
            }

            nav {
                padding: 10px;
                font-size: 1em;
            }

            nav a {
                display: block;
                margin: 10px 0;
            }

            .container {
                padding: 0 10px;
            }

            .about {
                flex-direction: column;
                text-align: center;
            }

            .about img {
                width: 100%;
                max-width: 100%;
                margin-bottom: 20px;
            }

            .services {
                grid-template-columns: 1fr;
            }

            .service {
                height: auto;
                padding: 20px;
            }

            .gallery {
                flex-direction: column;
            }

            .gallery img {
                width: 100%;
                height: auto;
            }

            .map {
                height: 300px;
            }

            .contact h2 {
                font-size: 2em;
            }

            .contact p {
                font-size: 1em;
            }

            .contact .social a {
                margin: 0 5px;
            }

            .contact .social img {
                height: 30px;
            }

            .testimonial {
                padding: 20px;
                flex-direction: column;
                align-items: center;
            }

            .testimonial img {
                height: 40px;
                margin-bottom: 10px;
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>Andi Irfan Maulana</h1>
        <p>Professional Car Sales Consultant</p>
    </header>

    <nav>
        <a href="#about">About Me</a>
        <a href="#services">Services</a>
        <a href="#gallery">Gallery</a>
        <a href="#testimonials">Testimonials</a>
        <a href="#contact">Contact</a>
    </nav>

    <div class="container">
        <section id="about" class="about">
            <img src="sales.jpg" alt="Profile Picture">
            <div>
                <h2>About Me</h2>
                <p>Hello, I'm Andi Irfan Maulana, a professional car sales consultant with over 10 years of experience in
                    the industry. I specialize in helping customers find the perfect vehicle that meets their needs and
                    budget.</p>
            </div>
        </section>

        <section id="services" class="services">
            <div class="service consult">
                <h3>Consultation</h3>
                <p>I offer personalized consultation to help you choose the right car that fits your lifestyle.</p>
            </div>
            <div class="service offer">
                <h3>Special Offers</h3>
                <p>Get access to exclusive deals and promotions on a wide range of vehicles.</p>
            </div>
            <div class="service test-drive">
                <h3>Test Drive</h3>
                <p>Schedule a test drive to experience the car before making a decision.</p>
            </div>
        </section>

        <section id="gallery" class="gallery">
            <img src="Zenix-Silver-p-1.png" alt="Gallery Image 1">
            <img src="hiace-premio.png" alt="Gallery Image 2">
            <img src="main_banner_toyota_new_fortuner_Attitude_Black.png" alt="Gallery Image 3">
        </section>

        <section id="testimonials" class="testimonials">
            <div class="testimonial">
                <img src="customer1.jpg" alt="Customer Photo">
                <p>"Andi is a fantastic consultant. He helped me find the perfect car within my budget. Highly
                    recommended!" - John Doe</p>
            </div>
            <div class="testimonial">
                <img src="customer2.jpg" alt="Customer Photo">
                <p>"I had a great experience working with Andi. He is very knowledgeable and patient." - Jane Smith</p>
            </div>
        </section>

        <iframe class="map"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3944.236567848016!2d115.21516501420998!3d-8.67045809093564!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd239d58a14d9f7%3A0xc0f87110a2295c7b!2sToyota%20Astra%20Motor%20Sanur!5e0!3m2!1sen!2sid!4v1613966484090!5m2!1sen!2sid"
            allowfullscreen="" loading="lazy"></iframe>

        <section id="contact" class="contact">
            <h2>Contact Me</h2>
            <p>Have any questions or need further assistance? Feel free to reach out to me!</p>
            <div class="social">
                <a href="#"><img src="facebook.png" alt="Facebook"></a>
                <a href="#"><img src="twitter.png" alt="Twitter"></a>
                <a href="#"><img src="instagram.png" alt="Instagram"></a>
            </div>
            <p>Email: andi.sales@example.com | Phone: +62 812-3456-7890</p>
        </section>
    </div>

    <footer>
        <p>&copy; 2023 Andi Irfan Maulana. All Rights Reserved.</p>
    </footer>
</body>

</html>
