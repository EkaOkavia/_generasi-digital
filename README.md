# _generasi-digital
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Co.PPI: Kopi Botolan Premium untuk Energi Otentikmu</title>
    <!-- Deskripsi untuk SEO, mengandung keyword utama -->
    <meta name="description" content="Nikmati kopi botolan premium Co.PPI dengan biji pilihan, tersedia varian Almond, Brown Sugar, dan Americano. Praktis dan segar, rasa kafe otentik di mana saja.">
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Lucide Icons untuk visual minimalis -->
    <script type="module">
        import { createIcons, Coffee, Zap, Leaf, Star, Truck, User } from 'https://unpkg.com/lucide@latest/dist/esm/lucide.js';
        createIcons({ icons: { Coffee, Zap, Leaf, Star, Truck, User } });
    </script>
    <style>
        /* Konfigurasi Warna Tailwind sesuai skema: */
        /* Dasar: #FAF0E6, Aksen: #E0B0B0, Teks: #4A2B2A, Sekunder: #D2B48C */
        :root {
            --color-base: #FAF0E6;
            --color-accent: #E0B0B0;
            --color-text: #4A2B2A;
            --color-secondary: #D2B48C;
        }
        .bg-base { background-color: var(--color-base); }
        .bg-accent { background-color: var(--color-accent); }
        .text-text { color: var(--color-text); }
        .text-accent { color: var(--color-accent); }
        .bg-secondary { background-color: var(--color-secondary); }
        
        /* Font Inter (default) */
        body {
            font-family: 'Inter', sans-serif;
            color: var(--color-text);
        }

        /* Styling tambahan untuk CTA utama */
        .cta-button {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .cta-button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
        }
    </style>
</head>
<body class="bg-base min-h-screen antialiased">

    <!-- 1. Header & Navigasi -->
    <header class="sticky top-0 z-50 bg-base/95 backdrop-blur-sm shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo -->
            <a href="#" class="text-3xl font-bold text-text">Co.PPI</a>
            
            <!-- Navigasi (Desktop) -->
            <nav class="hidden md:flex space-x-8 text-lg font-medium">
                <a href="#varian" class="hover:text-accent transition duration-200">Varian</a>
                <a href="#keunggulan" class="hover:text-accent transition duration-200">Keunggulan</a>
                <a href="#testimoni" class="hover:text-accent transition duration-200">Testimoni</a>
                <a href="#footer" class="hover:text-accent transition duration-200">Kontak</a>
            </nav>
            
            <!-- CTA Button (Primary - Header) -->
            <a href="#final-cta" class="hidden md:block bg-accent text-text font-semibold py-2 px-6 rounded-full cta-button">
                Pesan Sekarang
            </a>

            <!-- Mobile Menu Button (Placeholder) -->
            <button class="md:hidden text-text p-2 rounded-lg hover:bg-accent/30 transition">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-menu"><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
            </button>
        </div>
    </header>

    <main>
        <!-- 2. Hero Section (H1 - Wajib SEO) -->
        <section id="hero" class="pt-16 pb-24 bg-secondary/50">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid md:grid-cols-2 gap-12 items-center">
                <!-- Konten Teks -->
                <div class="space-y-6">
                    <!-- H1: Mengandung Keyword Utama -->
                    <h1 class="text-5xl md:text-6xl font-extrabold leading-tight text-text">
                        Co.PPI: <span class="text-accent">Kopi Botolan Premium</span> untuk Energi Otentikmu
                    </h1>
                    <!-- Sub-Headline -->
                    <p class="text-xl md:text-2xl text-text/80">
                        Nikmati kemudahan rasa kafe otentik di mana saja. Segar, praktis, dan dibuat dari biji pilihan.
                    </p>
                    
                    <!-- CTA Button (Primary) -->
                    <a href="#varian" class="inline-block bg-accent text-text font-bold text-xl py-4 px-10 rounded-xl cta-button mt-4">
                        Coba Rasa Favorit Anda!
                    </a>

                    <!-- Social Proof Kecil -->
                    <div class="flex items-center space-x-2 pt-4">
                        <div class="flex">
                            <!-- Ikon Bintang (5 Bintang) -->
                            <i data-lucide="star" class="w-5 h-5 fill-yellow-500 text-yellow-500"></i>
                            <i data-lucide="star" class="w-5 h-5 fill-yellow-500 text-yellow-500"></i>
                            <i data-lucide="star" class="w-5 h-5 fill-yellow-500 text-yellow-500"></i>
                            <i data-lucide="star" class="w-5 h-5 fill-yellow-500 text-yellow-500"></i>
                            <i data-lucide="star" class="w-5 h-5 fill-yellow-500 text-yellow-500"></i>
                        </div>
                        <span class="text-sm font-semibold text-text/70">4.9/5 dari 500+ Ulasan Puas</span>
                    </div>
                </div>

                <!-- Visual Produk -->
                <div class="relative flex justify-center md:justify-end">
                    <!-- Placeholder untuk gambar produk Co.PPI yang terlampir -->
                    <img src="https://placehold.co/600x400/D2B48C/4A2B2A?text=Foto+Produk+Co.PPI" 
                         alt="Empat botol kopi Co.PPI premium rasa Almond, Brown Sugar, dan Americano di atas meja kayu." 
                         class="w-full max-w-lg rounded-xl shadow-2xl transform hover:scale-[1.02] transition duration-500"
                         onerror="this.onerror=null; this.src='https://placehold.co/600x400/D2B48C/4A2B2A?text=Gambar+Produk';">
                </div>
            </div>
        </section>

        <!-- 3. Keunggulan Produk (Why Us?) -->
        <section id="keunggulan" class="py-20 bg-base">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <!-- H2 -->
                <h2 class="text-4xl font-bold mb-12">Kenapa Co.PPI Menjadi Pilihan Terbaik Anda?</h2>
                
                <div class="grid md:grid-cols-3 gap-8">
                    <!-- Keunggulan 1: Biji Pilihan Lokal (Keyword: Biji Kopi Arabika, Kopi Lokal) -->
                    <div class="bg-secondary/30 p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-[1.03]">
                        <i data-lucide="leaf" class="w-10 h-10 text-accent mx-auto mb-4"></i>
                        <h3 class="text-xl font-semibold mb-3">Biji Pilihan Lokal</h3>
                        <p class="text-text/80">Menggunakan 100% biji kopi Arabika dari petani terbaik di [Sebutkan Lokasi]. Rasa yang kaya dan berkelanjutan.</p>
                    </div>

                    <!-- Keunggulan 2: Sistem Brewing Cepat Dingin -->
                    <div class="bg-secondary/30 p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-[1.03]">
                        <i data-lucide="coffee" class="w-10 h-10 text-accent mx-auto mb-4"></i>
                        <h3 class="text-xl font-semibold mb-3">Brewing Cepat Dingin</h3>
                        <p class="text-text/80">Diproses dengan teknik *cold brew* modern untuk menjamin kesegaran maksimal dan rasa yang konsisten tanpa rasa pahit berlebih.</p>
                    </div>

                    <!-- Keunggulan 3: Praktis & Travel-Friendly -->
                    <div class="bg-secondary/30 p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-[1.03]">
                        <i data-lucide="truck" class="w-10 h-10 text-accent mx-auto mb-4"></i>
                        <h3 class="text-xl font-semibold mb-3">Praktis & *Travel-Friendly*</h3>
                        <p class="text-text/80">Kemasan botol yang aman dan tersegel rapat. Siap dinikmati di kantor, perjalanan, atau kapan pun Anda butuh *boost*.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. Varian Produk & Detail (Keyword Density) -->
        <section id="varian" class="py-20 bg-secondary/10">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <!-- H2 -->
                <h2 class="text-4xl font-bold mb-12">Jelajahi Pilihan Rasa Otentik Co.PPI</h2>
                
                <div class="grid md:grid-cols-3 gap-8">
                    <!-- Varian 1: Almond (H3, Keyword: Kopi Susu Almond) -->
                    <div class="bg-base p-6 rounded-xl shadow-xl border-t-4 border-accent">
                        <img src="https://placehold.co/300x300/F0E6D2/4A2B2A?text=ALMOND" 
                             alt="Botol Co.PPI rasa Almond." 
                             class="w-full h-auto object-cover rounded-lg mb-4">
                        <h3 class="text-2xl font-bold mb-2 text-accent">1. Almond</h3>
                        <p class="text-text/80">*Deskripsi:* Perpaduan lembut kopi dengan susu almond yang *creamy*. Alternatif rendah laktosa yang lezat. <span class="font-semibold">(Kopi Susu Almond Favorit)</span></p>
                    </div>

                    <!-- Varian 2: Brown Sugar (H3, Keyword: Kopi Gula Aren) -->
                    <div class="bg-base p-6 rounded-xl shadow-xl border-t-4 border-accent">
                        <img src="https://placehold.co/300x300/D2B48C/4A2B2A?text=BROWN+SUGAR" 
                             alt="Botol Co.PPI rasa Brown Sugar." 
                             class="w-full h-auto object-cover rounded-lg mb-4">
                        <h3 class="text-2xl font-bold mb-2 text-accent">2. Brown Sugar</h3>
                        <p class="text-text/80">*Deskripsi:* Klasik dan manis dengan sentuhan gula aren premium Indonesia. Rasa nostalgia yang memuaskan. <span class="font-semibold">(Kopi Gula Aren Autentik)</span></p>
                    </div>

                    <!-- Varian 3: Americano (H3, Keyword: Americano Botolan) -->
                    <div class="bg-base p-6 rounded-xl shadow-xl border-t-4 border-accent">
                        <img src="https://placehold.co/300x300/4A2B2A/FAF0E6?text=AMERICANO" 
                             alt="Botol Co.PPI rasa Americano." 
                             class="w-full h-auto object-cover rounded-lg mb-4">
                        <h3 class="text-2xl font-bold mb-2 text-accent">3. Americano</h3>
                        <p class="text-text/80">*Deskripsi:* Murni, kuat, dan menyegarkan. Pilihan tepat untuk Anda yang menyukai *black coffee* tanpa pemanis. <span class="font-semibold">(Americano Botolan Siap Minum)</span></p>
                    </div>
                </div>

                <!-- CTA Sekunder -->
                <a href="#" class="mt-10 inline-block text-lg font-semibold text-text hover:text-accent border-b-2 border-text hover:border-accent transition duration-300">
                    Lihat Komposisi Lengkap dan Informasi Nutrisi →
                </a>
            </div>
        </section>

        <!-- 5. Social Proof / Testimoni -->
        <section id="testimoni" class="py-20 bg-base">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <!-- H2 -->
                <h2 class="text-4xl font-bold mb-12">Ratusan Pelanggan Telah Jatuh Cinta</h2>
                
                <!-- Slider Testimoni (Sederhana) -->
                <div class="overflow-hidden relative">
                    <div class="flex space-x-6">
                        <!-- Ulasan 1 -->
                        <div class="min-w-full bg-secondary/50 p-8 rounded-xl shadow-lg border-l-4 border-accent text-left">
                            <div class="flex text-yellow-500 mb-3">
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                            </div>
                            <p class="italic text-lg mb-4 text-text">"Brown Sugar-nya pas banget manisnya, tidak bikin eneg. Jadi andalan saya setiap meeting pagi!"</p>
                            <p class="font-semibold text-text">- Rina S., Manajer Proyek</p>
                        </div>

                        <!-- Ulasan 2 -->
                        <div class="min-w-full bg-secondary/50 p-8 rounded-xl shadow-lg border-l-4 border-accent text-left">
                            <div class="flex text-yellow-500 mb-3">
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                                <i data-lucide="star" class="w-5 h-5 fill-yellow-500"></i>
                            </div>
                            <p class="italic text-lg mb-4 text-text">"Susu Almond-nya *creamy* tapi tetap ringan. Saya tidak bisa minum kopi susu biasa, Co.PPI solusinya!"</p>
                            <p class="font-semibold text-text">- Bima K., Pekerja Kreatif</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 6. Final Call-to-Action (The Closing Pitch) -->
        <section id="final-cta" class="py-24 bg-accent/70">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <!-- H2 -->
                <h2 class="text-4xl md:text-5xl font-extrabold mb-4 text-text">
                    Waktunya *Recharge* Energimu.
                </h2>
                <p class="text-xl md:text-2xl font-semibold mb-8 text-text/90">
                    Diskon <span class="text-red-700 font-extrabold">15%</span> untuk pembelian paket *bundling* rasa favorit, hanya berlaku hari ini!
                </p>
                
                <!-- CTA Button (Primary, Large) -->
                <a href="#" class="inline-block bg-text text-base font-bold text-xl py-4 px-12 rounded-full cta-button border-4 border-text hover:border-base hover:bg-base hover:text-text transition duration-300">
                    Pesan Sekarang dan Klaim Diskon Anda
                </a>
            </div>
        </section>
    </main>

    <!-- 7. Footer -->
    <footer id="footer" class="bg-text text-base py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-2 md:grid-cols-4 gap-8 text-base/90">
            
            <!-- Kolom 1: Logo & Kontak -->
            <div>
                <h3 class="text-2xl font-bold text-base mb-4">Co.PPI</h3>
                <p>Kopi premium botolan, dibuat untuk kesegaran harian Anda.</p>
                <div class="mt-4 space-y-1">
                    <p>Email: <a href="mailto:halo@coppi.id" class="hover:text-accent transition">halo@coppi.id</a></p>
                    <p>Telepon: <a href="tel:+628123456789" class="hover:text-accent transition">+62 812-3456-789</a></p>
                    <p>Alamat: Jl. Kopi Nikmat No. 12, Jakarta</p>
                </div>
            </div>

            <!-- Kolom 2: Navigasi Cepat -->
            <div>
                <h4 class="text-xl font-semibold text-base mb-4">Menu</h4>
                <ul class="space-y-2">
                    <li><a href="#varian" class="hover:text-accent transition">Varian Produk</a></li>
                    <li><a href="#keunggulan" class="hover:text-accent transition">Keunggulan Kami</a></li>
                    <li><a href="#testimoni" class="hover:text-accent transition">Testimoni</a></li>
                    <li><a href="#" class="hover:text-accent transition">FAQ</a></li>
                </ul>
            </div>

            <!-- Kolom 3: Legal & Info -->
            <div>
                <h4 class="text-xl font-semibold text-base mb-4">Informasi</h4>
                <ul class="space-y-2">
                    <li><a href="#" class="hover:text-accent transition">Syarat & Ketentuan</a></li>
                    <li><a href="#" class="hover:text-accent transition">Kebijakan Privasi</a></li>
                    <li><a href="#" class="hover:text-accent transition">Karir</a></li>
                </ul>
            </div>

            <!-- Kolom 4: Media Sosial -->
            <div>
                <h4 class="text-xl font-semibold text-base mb-4">Ikuti Kami</h4>
                <div class="flex space-x-4">
                    <!-- Ikon Sosial Media (Placeholder) -->
                    <a href="#" class="hover:text-accent transition"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-instagram"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg></a>
                    <a href="#" class="hover:text-accent transition"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-facebook"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg></a>
                    <a href="#" class="hover:text-accent transition"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-tiktok"><path d="M21 8a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h4l-1 4h-2"/><path d="M14 8v12h4v-8a4 4 0 0 0-4-4z"/></svg></a>
                </div>
            </div>
        </div>

        <div class="mt-8 pt-6 border-t border-base/20 text-center text-sm text-base/50">
            © 2024 Co.PPI - Semua Hak Cipta Dilindungi. Dibuat dengan cinta untuk pecinta kopi.
        </div>
    </footer>

</body>
</html>
