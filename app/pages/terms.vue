<script setup>
useHead({
  title: 'Terms of Service - WA Scheduler',
  meta: [
    { name: 'description', content: 'Syarat dan ketentuan penggunaan layanan WA Scheduler' }
  ]
})
</script>

<style scoped>
@keyframes pulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.6; }
}

.animate-pulse {
  animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

ul {
  list-style-type: disc;
}

ul li {
  margin-bottom: 0.5rem;
}
</style> 

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 relative overflow-hidden">
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute -top-40 -right-40 w-80 h-80 bg-purple-500 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-pulse"></div>
      <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-blue-500 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-pulse"></div>
    </div>

    <!-- Navigation -->
    <nav class="relative z-20 px-6 py-4">
      <div class="max-w-7xl mx-auto flex items-center justify-between">
        <NuxtLink to="/" class="flex items-center space-x-3">
          <div class="w-10 h-10 bg-gradient-to-r from-green-400 to-blue-500 rounded-xl flex items-center justify-center relative">
            <div class="w-6 h-6 bg-white rounded-lg flex items-center justify-center">
              <div class="w-4 h-4 grid grid-cols-2 gap-0.5">
                <div class="w-1 h-1 bg-green-500 rounded-sm"></div>
                <div class="w-1 h-1 bg-blue-500 rounded-sm"></div>
                <div class="w-1 h-1 bg-purple-500 rounded-sm"></div>
                <div class="w-1 h-1 bg-green-500 rounded-sm"></div>
              </div>
            </div>
            <div class="absolute -bottom-1 -right-1 w-2 h-2 bg-white transform rotate-45"></div>
          </div>
          <span class="text-xl font-bold text-white">WA Scheduler</span>
        </NuxtLink>
        
        <NuxtLink to="/" class="text-white/80 hover:text-white transition-colors">
          ← Kembali
        </NuxtLink>
      </div>
    </nav>

    <!-- Content -->
    <div class="relative z-10 px-6 py-12">
      <div class="max-w-4xl mx-auto">
        <!-- Header -->
        <div class="text-center mb-12">
          <h1 class="text-4xl lg:text-5xl font-bold text-white mb-4">
            Terms of <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">Service</span>
          </h1>
          <!-- <p class="text-white/60">Terakhir diperbarui: 3 Oktober 2025</p> -->
        </div>

        <!-- Content Card -->
        <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-3xl p-8 lg:p-12">
          <div class="prose prose-invert prose-lg max-w-none">
            
            <div class="backdrop-blur-md bg-blue-500/10 border border-blue-400/30 rounded-2xl p-6 mb-8">
              <p class="text-white/90 font-medium">
                Dengan menggunakan WA Scheduler, Anda menyetujui untuk terikat oleh syarat dan ketentuan ini. 
                Harap baca dengan seksama sebelum menggunakan layanan kami.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">1. Penerimaan Syarat</h2>
              <p class="text-white/80">
                Dengan mengakses dan menggunakan layanan WA Scheduler ("Layanan"), Anda menyetujui untuk terikat 
                oleh Syarat dan Ketentuan ini dan semua hukum dan peraturan yang berlaku. 
                Jika Anda tidak setuju dengan salah satu syarat ini, Anda dilarang menggunakan atau mengakses Layanan ini.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">2. Deskripsi Layanan</h2>
              <p class="text-white/80 mb-4">
                WA Scheduler menyediakan layanan bot WhatsApp untuk manajemen jadwal dan pengingat. Layanan kami meliputi:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Pembuatan dan pengelolaan event/jadwal</li>
                <li>Pengiriman reminder otomatis</li>
                <li>Motivasi harian yang dapat disesuaikan</li>
                <li>Integrasi dengan WhatsApp</li>
                <li>Fitur AI untuk pemrosesan bahasa natural</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">3. Akun Pengguna</h2>
              <p class="text-white/80 mb-4">
                Untuk menggunakan layanan kami, Anda harus:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Berusia minimal 13 tahun</li>
                <li>Memiliki akun WhatsApp yang valid</li>
                <li>Memberikan informasi yang akurat dan lengkap saat registrasi</li>
                <li>Menjaga keamanan akun Anda</li>
                <li>Bertanggung jawab atas semua aktivitas yang terjadi di bawah akun Anda</li>
              </ul>
              <p class="text-white/80 mt-4">
                Anda tidak boleh berbagi akun Anda dengan orang lain atau menggunakan akun orang lain tanpa izin.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">4. Penggunaan yang Dapat Diterima</h2>
              <p class="text-white/80 mb-4">Anda setuju untuk TIDAK:</p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Menggunakan layanan untuk tujuan ilegal atau tidak sah</li>
                <li>Mengirim spam, konten berbahaya, atau malware</li>
                <li>Melanggar hak kekayaan intelektual pihak lain</li>
                <li>Mencoba mengakses sistem kami secara tidak sah</li>
                <li>Mengganggu atau merusak layanan atau server kami</li>
                <li>Menggunakan bot atau script otomatis tanpa izin</li>
                <li>Menyalahgunakan fitur AI untuk konten yang tidak pantas</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">5. Konten Pengguna</h2>
              <p class="text-white/80 mb-4">
                Anda mempertahankan kepemilikan atas konten yang Anda buat menggunakan layanan kami. 
                Namun, dengan menggunakan layanan kami, Anda memberikan kami lisensi untuk:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Menyimpan dan memproses konten Anda untuk menyediakan layanan</li>
                <li>Menggunakan data agregat untuk meningkatkan layanan</li>
                <li>Menampilkan konten Anda kembali kepada Anda</li>
              </ul>
              <p class="text-white/80 mt-4">
                Anda bertanggung jawab penuh atas konten yang Anda buat dan harus memastikan bahwa 
                Anda memiliki hak untuk menggunakan konten tersebut.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">6. Ketersediaan Layanan</h2>
              <p class="text-white/80">
                Kami berusaha untuk menjaga layanan tersedia 24/7, namun kami tidak menjamin bahwa layanan 
                akan selalu tersedia tanpa gangguan. Kami dapat:
              </p>
              <ul class="text-white/80 space-y-2 ml-6 mt-4">
                <li>Melakukan pemeliharaan terjadwal atau darurat</li>
                <li>Memodifikasi atau menghentikan layanan (atau bagian darinya)</li>
                <li>Membatasi akses selama periode beban tinggi</li>
              </ul>
              <p class="text-white/80 mt-4">
                Kami tidak bertanggung jawab atas kerugian yang timbul dari ketidaktersediaan layanan.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">7. Biaya dan Pembayaran</h2>
              <p class="text-white/80 mb-4">
                Layanan dasar WA Scheduler saat ini gratis. Jika kami memperkenalkan fitur berbayar di masa depan:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Anda akan diberi tahu terlebih dahulu tentang perubahan harga</li>
                <li>Pembayaran akan diproses melalui penyedia pembayaran pihak ketiga yang aman</li>
                <li>Pengembalian dana akan tunduk pada kebijakan pengembalian dana kami</li>
                <li>Anda bertanggung jawab atas semua pajak yang berlaku</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">8. Kekayaan Intelektual</h2>
              <p class="text-white/80">
                Semua hak kekayaan intelektual dalam layanan, termasuk tetapi tidak terbatas pada 
                perangkat lunak, desain, logo, dan konten, adalah milik WA Scheduler atau pemberi lisensi kami. 
                Anda tidak boleh menyalin, memodifikasi, mendistribusikan, atau membuat karya turunan 
                dari materi apa pun tanpa izin tertulis.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">9. Penghentian</h2>
              <p class="text-white/80 mb-4">
                Kami berhak untuk menangguhkan atau menghentikan akun Anda jika:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Anda melanggar Syarat dan Ketentuan ini</li>
                <li>Kami mencurigai aktivitas penipuan atau ilegal</li>
                <li>Kami diharuskan oleh hukum</li>
                <li>Anda tidak aktif untuk jangka waktu yang lama</li>
              </ul>
              <p class="text-white/80 mt-4">
                Anda dapat menghentikan akun Anda kapan saja dengan menghubungi dukungan kami 
                atau melalui pengaturan akun.
              </p>
            </div>

            <div class="backdrop-blur-md bg-green-500/10 border border-green-400/30 rounded-2xl p-6">
              <h2 class="text-2xl font-bold text-white mb-4">📞 Pertanyaan?</h2>
              <p class="text-white/80 mb-4">
                Jika Anda memiliki pertanyaan tentang Syarat dan Ketentuan ini, silakan hubungi kami:
              </p>
              <div class="text-white/80 space-y-2">
                <p>📧 Email: ramadifan769@gmail.com</p>
                <p>📱 WhatsApp: +62 858-9108-8596</p>
              </div>
            </div>

          </div>
        </div>

        <!-- Back Button -->
        <div class="text-center mt-8">
          <NuxtLink 
            to="/" 
            class="inline-flex items-center bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 text-white px-8 py-3 rounded-full font-semibold transition-all transform hover:scale-105"
          >
            ← Kembali ke Beranda
          </NuxtLink>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="relative z-10 px-6 py-8 mt-12 border-t border-white/10">
      <div class="max-w-7xl mx-auto text-center text-white/60">
        <p>© 2025 WA Scheduler. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>
