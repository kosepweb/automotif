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

        @media (max-width: 768px) {
            .about {
                flex-direction: column;
            }

            .about img {
                margin-bottom: 20px;
            }

            .gallery {
                flex-direction: column;
            }
        }
    </style>

    <!-- Background Music -->
    <audio autoplay loop>
        <source src="semangat.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <!-- Navigation -->
    <nav>
        <a href="#about">Tentang Saya</a>
        <a href="#services">Layanan</a>
        <a href="#gallery">Galeri</a>
        <a href="#testimonials">Testimoni</a>
        <a href="#contact">Hubungi Saya</a>
    </nav>

    <!-- Header -->
    <header>
        <h1>Andi Irfan Maulana</h1>
        <p>Sales Mobil Profesional Andalanta</p>
    </header>

    <div class="container">
        <!-- About Section -->
        <section id="about" class="about">
            <img src="sales.jpg" alt="Andi Irfan Maulana">
            <div>
                <h2>Tentang Saya</h2>
                <p>Selamat datang di profil saya! Saya Andi Irfan Maulana, seorang sales mobil dengan pengalaman lebih dari 10 tahun dalam industri otomotif. Saya berkomitmen untuk membantu Anda menemukan mobil impian Anda dan memberikan pelayanan terbaik.</p>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="services">
            <div class="service consult" style="background-image: url('sales2.jpg');">
                <h3>Konsultasi Pembelian</h3>
                <p>Saya akan membantu Anda memilih mobil yang sesuai dengan kebutuhan dan anggaran Anda.</p>
            </div>
            <div class="service offer" style="background-image: url('penawaran.jpg');">
                <h3>Penawaran Terbaik</h3>
                <p>Saya menyediakan berbagai penawaran dan diskon eksklusif untuk pembelian mobil baru.</p>
            </div>
            <div class="service test-drive" style="background-image: url('tes.jpg');">
                <h3>Test Drive</h3>
                <p>Rasakan langsung kenyamanan dan performa mobil pilihan Anda dengan layanan test drive kami.</p>
            </div>
        </section>

        <!-- Gallery Section -->
        <section id="gallery">
            <h2>Galeri Promosi</h2>
            <div class="gallery">
                <img src="foto1.jpg" alt="Promo 1" data-caption="Promo 1 Description">
                <img src="foto2.png" alt="Promo 2" data-caption="Promo 2 Description">
                <img src="foto3.jpg" alt="Promo 3" data-caption="Promo 3 Description">
                <img src="foto4.png" alt="Promo 4" data-caption="Promo 4 Description">
            </div>
        </section>

        <!-- Testimonials Section -->
        <section id="Kerjasama">
            <h2>Kerjasama</h2>
        <section id="testimonials" class="testimonials">
            <div class="testimonial">
                <p>"Kami bekerjasama dengan beberapa pihak pembiayaan."</p>
                <div class="author-logos">
                    <img src="bfi.jpeg" alt="BFI Logo">
                    <img src="adira.png" alt="Adira Logo">
                    <img src="mandiri.png.crdownload" alt="Mandiri Logo">
                    <img src="oto.jpeg" alt="Oto Logo">
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact">
            <h2>Hubungi Saya</h2>
            <p>Saya siap membantu Anda. Jangan ragu untuk menghubungi saya untuk konsultasi atau pertanyaan lebih lanjut.</p>
            <div class="social">
                <a href="https://wa.me/+6285345674445" target="_blank" title="Hubungi via WhatsApp">
                    <img src="wa.png" alt="WhatsApp Logo">
                </a>
                <a href="https://instagram.com/andiirfanmaulana" target="_blank" title="Lihat Instagram">
                    <img src="ig.png.crdownload" alt="Instagram Logo">
                </a>
            </div>
            <p>Alamat: Jln. Tamalanrea BTP , Kota Makassar</p>
            <a href="https://www.google.com/maps/place/Jl.+Kesenangan+3,+Tamalanrea,+Kec.+Tamalanrea,+Kota+Makassar,+Sulawesi+Selatan+90245/@-5.1321812,119.4988383,17z/data=!3m1!4b1!4m6!3m5!1s0x2dbefcb1d60774cb:0x9e04f396881d124a!8m2!3d-5.1321812!4d119.5014132!16s%2Fg%2F1hm64_pkm?entry=ttu&g_ep=EgoyMDI0MDgyMS4wIKXMDSoASAFQAw%3D%3D" target="_blank" title="Lihat di Google Maps">Lihat di Google Maps</a>
            <!-- Embedding Google Maps -->
            <iframe class="map" src="https://www.google.com/maps/place/Jl.+Kesenangan+3,+Tamalanrea,+Kec.+Tamalanrea,+Kota+Makassar,+Sulawesi+Selatan+90245/@-5.1321812,119.4988329,17z/data=!3m1!4b1!4m6!3m5!1s0x2dbefcb1d60774cb:0x9e04f396881d124a!8m2!3d-5.1321812!4d119.5014132!16s%2Fg%2F1hm64_pkm?entry=ttu&g_ep=EgoyMDI0MDgyMS4wIKXMDSoASAFQAw%3D%3D" allowfullscreen="" loading="lazy"></iframe>
        </section>
    </div>

    <!-- Gallery Modal -->
    <div class="gallery-item" id="gallery-item">
        <span class="close" onclick="closeGallery()">&times;</span>
        <img id="modal-img" src="" alt="Expanded Image">
        <div class="caption" id="modal-caption"></div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Andi Irfan Maulana. All Rights Reserved.</p>
    </footer>

    <script>
        document.querySelectorAll('.gallery img').forEach(img => {
            img.addEventListener('click', function () {
                const modal = document.getElementById('gallery-item');
                const modalImg = document.getElementById('modal-img');
                const modalCaption = document.getElementById('modal-caption');
                
                modal.style.display = 'flex';
                modalImg.src = this.src;
                modalCaption.textContent = this.dataset.caption;
            });
        });

        function closeGallery() {
            document.getElementById('gallery-item').style.display = 'none';
        }
    </script>
</body>

</html>
