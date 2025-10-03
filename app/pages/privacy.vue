<!-- pages/privacy.vue -->
<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 relative overflow-hidden">
    <!-- Background Animated Elements -->
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
            Privacy <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">Policy</span>
          </h1>
        </div>

        <!-- Content Card -->
        <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-3xl p-8 lg:p-12">
          <div class="prose prose-invert prose-lg max-w-none">
            
            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">1. Informasi yang Kami Kumpulkan</h2>
              <p class="text-white/80 mb-4">
                Kami mengumpulkan informasi yang Anda berikan secara langsung kepada kami, termasuk:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Nomor telepon WhatsApp Anda</li>
                <li>Nama dan informasi profil</li>
                <li>Jadwal dan event yang Anda buat</li>
                <li>Pesan dan interaksi dengan bot</li>
                <li>Preferensi dan pengaturan akun</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">2. Bagaimana Kami Menggunakan Informasi Anda</h2>
              <p class="text-white/80 mb-4">
                Informasi yang kami kumpulkan digunakan untuk:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Menyediakan, memelihara, dan meningkatkan layanan kami</li>
                <li>Mengirimkan reminder dan notifikasi event</li>
                <li>Memproses permintaan dan perintah Anda</li>
                <li>Berkomunikasi dengan Anda tentang layanan kami</li>
                <li>Menganalisis penggunaan untuk meningkatkan pengalaman pengguna</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">3. Keamanan Data</h2>
              <p class="text-white/80 mb-4">
                Kami menggunakan langkah-langkah keamanan teknis dan organisasi yang sesuai untuk melindungi data pribadi Anda:
              </p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Enkripsi end-to-end untuk semua komunikasi</li>
                <li>Server yang aman dengan akses terbatas</li>
                <li>Pemantauan keamanan 24/7</li>
                <li>Backup data secara regular</li>
                <li>Audit keamanan berkala</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">4. Berbagi Informasi</h2>
              <p class="text-white/80">
                Kami tidak menjual, memperdagangkan, atau mentransfer informasi pribadi Anda kepada pihak ketiga tanpa persetujuan Anda.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">5. Hak Anda</h2>
              <p class="text-white/80 mb-4">Anda memiliki hak untuk:</p>
              <ul class="text-white/80 space-y-2 ml-6">
                <li>Mengakses data pribadi Anda</li>
                <li>Memperbaiki data yang tidak akurat</li>
                <li>Menghapus data Anda (right to be forgotten)</li>
                <li>Membatasi pemrosesan data Anda</li>
                <li>Memindahkan data Anda (portabilitas data)</li>
                <li>Menolak pemrosesan data Anda</li>
              </ul>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">6. Penyimpanan Data</h2>
              <p class="text-white/80">
                Kami menyimpan data pribadi Anda selama akun Anda aktif atau selama diperlukan untuk menyediakan layanan. 
                Anda dapat menghapus akun Anda kapan saja, dan kami akan menghapus data Anda dalam waktu 30 hari, 
                kecuali jika diwajibkan oleh hukum untuk menyimpannya lebih lama.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">7. Cookie dan Teknologi Pelacakan</h2>
              <p class="text-white/80">
                Kami menggunakan cookie dan teknologi pelacakan serupa untuk meningkatkan pengalaman Anda, 
                menganalisis tren, dan mengumpulkan informasi demografis tentang basis pengguna kami secara keseluruhan.
              </p>
            </div>

            <div class="mb-8">
              <h2 class="text-2xl font-bold text-white mb-4">8. Privasi Anak-anak</h2>
              <p class="text-white/80">
                Layanan kami tidak ditujukan untuk anak-anak di bawah usia 13 tahun. 
                Kami tidak secara sengaja mengumpulkan informasi pribadi dari anak-anak di bawah 13 tahun. 
                Jika Anda mengetahui bahwa anak Anda telah memberikan kami informasi pribadi, 
                silakan hubungi kami segera.
              </p>
            </div>

            <div class="backdrop-blur-md bg-green-500/10 border border-green-400/30 rounded-2xl p-6">
              <h2 class="text-2xl font-bold text-white mb-4">📞 Hubungi Kami</h2>
              <p class="text-white/80 mb-4">
                Jika Anda memiliki pertanyaan tentang kebijakan privasi ini atau praktik data kami, 
                silakan hubungi kami:
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

<script setup>
useHead({
  title: 'Privacy Policy - WA Scheduler',
  meta: [
    { name: 'description', content: 'Kebijakan privasi WA Scheduler - Bagaimana kami melindungi data pribadi Anda' }
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