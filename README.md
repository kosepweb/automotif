<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Sales Mobil - Andi Irfan Maulana</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
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
        }

        .testimonial p {
            font-style: italic;
            color: #666;
        }

        .testimonial .author-logos {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }

        .testimonial .author-logos img {
            height: 30px;
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
            }

            .testimonial .author-logos img {
                height: 20px;
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>Profil Sales Mobil</h1>
        <p>Andi Irfan Maulana - Penawaran Terbaik Untuk Anda</p>
    </header>

    <nav>
        <a href="#about">Tentang Kami</a>
        <a href="#services">Layanan</a>
        <a href="#gallery">Galeri</a>
        <a href="#testimonials">Testimoni</a>
        <a href="#contact">Hubungi Kami</a>
    </nav>

    <div class="container">
        <section id="about" class="about">
            <img src="foto3.jpg" alt="Foto Profil">
            <div>
                <h2>Tentang Kami</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vehicula urna sit amet magna
                    pretium, a commodo justo dictum. Aliquam erat volutpat. Mauris ac neque at ante cursus blandit
                    non a nunc.</p>
            </div>
        </section>

        <section id="services" class="services">
            <div class="service consult" style="background-image: url('sales2.jpg');">
                <h3>Konsultasi</h3>
                <p>Kami menyediakan konsultasi yang mendalam untuk membantu Anda menemukan mobil yang tepat.</p>
            </div>
            <div class="service offer" style="background-image: url('penawaran.jpg');">
                <h3>Penawaran Terbaik</h3>
                <p>Dapatkan penawaran terbaik untuk mobil baru dan bekas dari kami.</p>
            </div>
            <div class="service test-drive" style="background-image: url('tes.jpg');">
                <h3>Test Drive</h3>
                <p>Jadwalkan test drive dan rasakan pengalaman berkendara yang sebenarnya.</p>
            </div>
        </section>

        <section id="gallery">
            <h2>Galeri</h2>
            <div class="gallery">
                <img src="mobil1.jpg" alt="Mobil 1" onclick="openGallery(this)">
                <img src="mobil2.jpg" alt="Mobil 2" onclick="openGallery(this)">
                <img src="mobil3.jpg" alt="Mobil 3" onclick="openGallery(this)">
                <!-- Tambahkan gambar lain sesuai kebutuhan -->
            </div>
        </section>

        <section id="testimonials" class="testimonials">
            <div class="testimonial">
                <p>"Layanan yang sangat profesional! Saya sangat puas dengan pembelian mobil saya."</p>
                <div class="author-logos">
                    <img src="logo1.png" alt="Logo Penulis">
                </div>
            </div>
            <div class="testimonial">
                <p>"Prosesnya sangat mudah dan cepat. Terima kasih atas bantuannya!"</p>
                <div class="author-logos">
                    <img src="logo2.png" alt="Logo Penulis">
                </div>
            </div>
            <!-- Tambahkan testimonial lain sesuai kebutuhan -->
        </section>

        <section id="contact" class="contact">
            <h2>Hubungi Kami</h2>
            <p>Jika Anda memiliki pertanyaan atau ingin menjadwalkan konsultasi, silakan hubungi kami.</p>
            <div class="social">
                <a href="https://wa.me/1234567890" target="_blank"><img src="whatsapp.png" alt="WhatsApp"></a>
                <a href="https://instagram.com/yourprofile" target="_blank"><img src="instagram.png" alt="Instagram"></a>
            </div>
            <p>Alamat: Jl. Contoh No.123, Jakarta</p>
            <iframe class="map" src="https://www.google.com/maps/embed?pb=..." allowfullscreen></iframe>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 Andi Irfan Maulana. Semua hak cipta dilindungi.</p>
    </footer>

    <!-- Gallery Modal -->
    <div id="gallery-modal" class="gallery-item">
        <span class="close" onclick="closeGallery()">&times;</span>
        <img id="modal-img" src="" alt="Gallery Item">
        <div class="caption" id="modal-caption"></div>
    </div>

    <script>
        function openGallery(img) {
            var modal = document.getElementById('gallery-modal');
            var modalImg = document.getElementById('modal-img');
            var captionText = document.getElementById('modal-caption');
            modal.style.display = 'flex';
            modalImg.src = img.src;
            captionText.innerHTML = img.alt;
        }

        function closeGallery() {
            var modal = document.getElementById('gallery-modal');
            modal.style.display = 'none';
        }
    </script>
</body>

</html>
