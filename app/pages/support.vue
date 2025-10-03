<!-- pages/support.vue -->
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
      <div class="max-w-6xl mx-auto">
        <!-- Header -->
        <div class="text-center mb-12">
          <h1 class="text-4xl lg:text-5xl font-bold text-white mb-4">
            Pusat <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">Bantuan</span>
          </h1>
          <p class="text-xl text-white/80">Kami siap membantu Anda 24/7</p>
        </div>

        <!-- Contact Cards -->
        <div class="grid md:grid-cols-3 gap-6 mb-12">
          <div class="backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 text-center transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-green-400 to-teal-400 rounded-2xl flex items-center justify-center mx-auto mb-4">
              <span class="text-3xl">📱</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-2">WhatsApp Support</h3>
            <p class="text-white/70 mb-4">Chat langsung dengan tim support</p>
            <a href="https://wa.me/6285891088596" target="_blank" class="inline-block bg-green-500 hover:bg-green-600 text-white px-6 py-2 rounded-full font-semibold transition-all">
              Chat Sekarang
            </a>
          </div>

          <div class="backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 text-center transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-blue-400 to-purple-400 rounded-2xl flex items-center justify-center mx-auto mb-4">
              <span class="text-3xl">📧</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-2">Email Support</h3>
            <p class="text-white/70 mb-4">Kirim pertanyaan detail Anda</p>
            <a href="mailto:ramadifan769@gmail.com" class="inline-block bg-blue-500 hover:bg-blue-600 text-white px-6 py-2 rounded-full font-semibold transition-all">
              Kirim Email
            </a>
          </div>

          <div class="backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 text-center transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-purple-400 to-pink-400 rounded-2xl flex items-center justify-center mx-auto mb-4">
              <span class="text-3xl">📚</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-2">Documentation</h3>
            <p class="text-white/70 mb-4">Panduan lengkap penggunaan</p>
            <a href="#faq" class="inline-block bg-purple-500 hover:bg-purple-600 text-white px-6 py-2 rounded-full font-semibold transition-all">
              Lihat Panduan
            </a>
          </div>
        </div>

        <!-- FAQ Section -->
        <div id="faq" class="backdrop-blur-md bg-white/5 border border-white/10 rounded-3xl p-8 lg:p-12 mb-12">
          <h2 class="text-3xl font-bold text-white mb-8 text-center">
            📋 Pertanyaan yang Sering Diajukan (FAQ)
          </h2>

          <div class="space-y-4">
            <!-- FAQ Item 1 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(0)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Bagaimana cara memulai menggunakan WA Scheduler?</span>
                <svg :class="openFaq === 0 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 0" class="px-6 pb-6">
                <p class="text-white/80">
                  Sangat mudah! Cukup klik tombol "Login / Register" di halaman utama, lalu ikuti instruksi untuk menghubungkan nomor WhatsApp Anda. 
                  Setelah terhubung, Anda bisa langsung mulai membuat jadwal dengan mengirim pesan ke bot seperti: 
                  "bikin meeting besok jam 2 siang".
                </p>
              </div>
            </div>

            <!-- FAQ Item 2 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(1)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Apakah layanan ini gratis?</span>
                <svg :class="openFaq === 1 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 1" class="px-6 pb-6">
                <p class="text-white/80">
                  Ya! WA Scheduler saat ini sepenuhnya gratis untuk digunakan. Anda dapat membuat jadwal unlimited, 
                  menerima reminder, dan menggunakan semua fitur AI tanpa biaya. Tidak ada biaya tersembunyi atau 
                  kartu kredit yang diperlukan untuk memulai.
                </p>
              </div>
            </div>

            <!-- FAQ Item 3 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(2)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Bagaimana cara membuat jadwal/event?</span>
                <svg :class="openFaq === 2 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 2" class="px-6 pb-6">
                <p class="text-white/80 mb-3">
                  Cukup chat dengan bot seperti ngobrol dengan teman! Contoh pesan:
                </p>
                <ul class="text-white/70 space-y-2 ml-6">
                  <li>• "bikin meeting besok jam 2 siang"</li>
                  <li>• "ingetin aku olahraga setiap senin rabu jumat jam 6 pagi"</li>
                  <li>• "buat event launching product tanggal 15 oktober jam 7 malam"</li>
                </ul>
                <p class="text-white/80 mt-3">
                  Bot AI kami akan memahami dan memproses permintaan Anda secara otomatis!
                </p>
              </div>
            </div>

            <!-- FAQ Item 4 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(3)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Bagaimana cara melihat semua jadwal saya?</span>
                <svg :class="openFaq === 3 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 3" class="px-6 pb-6">
                <p class="text-white/80 mb-3">
                  Anda bisa mengirim pesan seperti:
                </p>
                <ul class="text-white/70 space-y-2 ml-6">
                  <li>• "jadwal hari ini" - untuk melihat jadwal hari ini</li>
                  <li>• "jadwal minggu ini" - untuk melihat jadwal seminggu</li>
                  <li>• "jadwal bulan ini" - untuk melihat jadwal sebulan</li>
                  <li>• "lihat semua jadwal" - untuk melihat semua jadwal</li>
                </ul>
              </div>
            </div>

            <!-- FAQ Item 5 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(4)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Bagaimana cara mengedit atau menghapus event?</span>
                <svg :class="openFaq === 4 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 4" class="px-6 pb-6">
                <p class="text-white/80 mb-3">
                  Untuk mengedit event, kirim pesan seperti:
                </p>
                <ul class="text-white/70 space-y-2 ml-6 mb-3">
                  <li>• "edit event meeting jadi jam 3 sore"</li>
                  <li>• "ubah jadwal meeting ke tanggal 20"</li>
                </ul>
                <p class="text-white/80 mb-3">
                  Untuk menghapus event:
                </p>
                <ul class="text-white/70 space-y-2 ml-6">
                  <li>• "hapus event meeting"</li>
                  <li>• "cancel meeting besok"</li>
                </ul>
              </div>
            </div>

            <!-- FAQ Item 6 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(5)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Kapan saya akan menerima reminder?</span>
                <svg :class="openFaq === 5 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 5" class="px-6 pb-6">
                <p class="text-white/80">
                  Secara default, reminder akan dikirim 30 menit sebelum event dimulai. 
                  Anda akan menerima pesan WhatsApp yang berisi detail event dan persiapan yang perlu dilakukan. 
                  Anda juga bisa mengatur waktu reminder sesuai keinginan dengan mengirim pesan seperti: 
                  "ingetin 1 jam sebelumnya".
                </p>
              </div>
            </div>

            <!-- FAQ Item 7 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(6)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Apa itu fitur Motivasi Harian?</span>
                <svg :class="openFaq === 6 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 6" class="px-6 pb-6">
                <p class="text-white/80 mb-3">
                  Motivasi Harian adalah fitur yang mengirimkan pesan motivasi inspiratif setiap hari pada waktu yang Anda tentukan. 
                  Konten motivasi di-generate oleh AI dan selalu fresh setiap hari.
                </p>
                <p class="text-white/80 mb-3">
                  Untuk mengaktifkan: "kirim motivasi setiap hari jam 7 pagi"
                </p>
                <p class="text-white/80">
                  Untuk menonaktifkan: "stop motivasi harian"
                </p>
              </div>
            </div>

            <!-- FAQ Item 8 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(7)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Apakah data saya aman?</span>
                <svg :class="openFaq === 7 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 7" class="px-6 pb-6">
                <p class="text-white/80">
                  Sangat aman! Kami menggunakan enkripsi end-to-end untuk semua komunikasi dan data Anda disimpan 
                  di server yang aman dengan akses terbatas. Kami tidak pernah menjual atau membagikan data Anda 
                  kepada pihak ketiga tanpa izin Anda. Baca lebih lanjut di halaman Privacy Policy kami.
                </p>
              </div>
            </div>

            <!-- FAQ Item 9 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(8)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Bagaimana jika bot tidak mengerti pesan saya?</span>
                <svg :class="openFaq === 8 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 8" class="px-6 pb-6">
                <p class="text-white/80">
                  Bot kami menggunakan AI yang terus belajar, tapi jika bot tidak mengerti pesan Anda, 
                  coba rumuskan ulang dengan lebih spesifik. Contohnya, daripada "nanti sore", 
                  lebih baik "hari ini jam 4 sore". Jika masih ada masalah, tim support kami siap membantu!
                </p>
              </div>
            </div>

            <!-- FAQ Item 10 -->
            <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-2xl overflow-hidden">
              <button @click="toggleFaq(9)" class="w-full p-6 text-left flex items-center justify-between hover:bg-white/5 transition-all">
                <span class="text-lg font-semibold text-white">Apakah saya bisa menggunakan WA Scheduler untuk tim/perusahaan?</span>
                <svg :class="openFaq === 9 ? 'rotate-180' : ''" class="w-6 h-6 text-white transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 9" class="px-6 pb-6">
                <p class="text-white/80">
                  Tentu saja! WA Scheduler cocok untuk penggunaan personal maupun tim. 
                  Untuk kebutuhan enterprise dengan fitur tambahan seperti multi-user management, 
                  team collaboration, dan custom integration, silakan hubungi tim support kami di 
                  ramadifan769@gmail.com
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="backdrop-blur-md bg-white/5 border border-white/10 rounded-3xl p-8 lg:p-12">
          <h2 class="text-3xl font-bold text-white mb-6 text-center">
            💬 Masih Punya Pertanyaan?
          </h2>
          <p class="text-white/70 text-center mb-8">
            Kirim pesan kepada kami dan kami akan merespon secepat mungkin
          </p>

          <form @submit.prevent="handleSubmit" class="max-w-2xl mx-auto space-y-6">
            <div>
              <label class="block text-white font-medium mb-2">Nama</label>
              <input 
                v-model="form.name"
                type="text" 
                required
                class="w-full bg-white/5 border border-white/20 rounded-xl px-4 py-3 text-white placeholder-white/40 focus:outline-none focus:border-green-400 transition-colors"
                placeholder="Nama Anda"
              >
            </div>

            <div>
              <label class="block text-white font-medium mb-2">Email</label>
              <input 
                v-model="form.email"
                type="email" 
                required
                class="w-full bg-white/5 border border-white/20 rounded-xl px-4 py-3 text-white placeholder-white/40 focus:outline-none focus:border-green-400 transition-colors"
                placeholder="email@example.com"
              >
            </div>

            <div>
              <label class="block text-white font-medium mb-2">Nomor WhatsApp</label>
              <input 
                v-model="form.phone"
                type="tel" 
                class="w-full bg-white/5 border border-white/20 rounded-xl px-4 py-3 text-white placeholder-white/40 focus:outline-none focus:border-green-400 transition-colors"
                placeholder="+62 812-3456-7890"
              >
            </div>

            <div>
              <label class="block text-white font-medium mb-2">Kategori</label>
              <select 
                v-model="form.category"
                required
                class="w-full bg-white/5 border border-white/20 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-green-400 transition-colors"
              >
                <option value="" disabled>Pilih kategori</option>
                <option value="technical">Masalah Teknis</option>
                <option value="account">Akun & Login</option>
                <option value="feature">Pertanyaan Fitur</option>
                <option value="billing">Billing & Pembayaran</option>
                <option value="feedback">Feedback & Saran</option>
                <option value="other">Lainnya</option>
              </select>
            </div>

            <div>
              <label class="block text-white font-medium mb-2">Pesan</label>
              <textarea 
                v-model="form.message"
                required
                rows="5"
                class="w-full bg-white/5 border border-white/20 rounded-xl px-4 py-3 text-white placeholder-white/40 focus:outline-none focus:border-green-400 transition-colors resize-none"
                placeholder="Ceritakan masalah atau pertanyaan Anda..."
              ></textarea>
            </div>

            <button 
              type="submit"
              :disabled="isSubmitting"
              class="w-full bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 disabled:from-gray-500 disabled:to-gray-600 text-white px-8 py-4 rounded-xl font-bold text-lg transition-all transform hover:scale-105 disabled:scale-100 disabled:cursor-not-allowed"
            >
              {{ isSubmitting ? '⏳ Mengirim...' : '📤 Kirim Pesan' }}
            </button>

            <div v-if="submitMessage" class="text-center p-4 rounded-xl" :class="submitSuccess ? 'bg-green-500/20 text-green-300 border border-green-400/30' : 'bg-red-500/20 text-red-300 border border-red-400/30'">
              {{ submitMessage }}
            </div>
          </form>
        </div>

        <!-- Additional Resources -->
        <div class="grid md:grid-cols-2 gap-6 mt-12">
          <NuxtLink to="/privacy" class="backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-6 transition-all hover:-translate-y-1">
            <div class="flex items-center space-x-4">
              <div class="w-12 h-12 bg-gradient-to-r from-blue-400 to-purple-400 rounded-xl flex items-center justify-center">
                <span class="text-2xl">🔒</span>
              </div>
              <div>
                <h3 class="text-lg font-bold text-white mb-1">Privacy Policy</h3>
                <p class="text-white/60 text-sm">Lihat bagaimana kami melindungi data Anda</p>
              </div>
            </div>
          </NuxtLink>

          <NuxtLink to="/terms" class="backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-6 transition-all hover:-translate-y-1">
            <div class="flex items-center space-x-4">
              <div class="w-12 h-12 bg-gradient-to-r from-purple-400 to-pink-400 rounded-xl flex items-center justify-center">
                <span class="text-2xl">📄</span>
              </div>
              <div>
                <h3 class="text-lg font-bold text-white mb-1">Terms of Service</h3>
                <p class="text-white/60 text-sm">Baca syarat dan ketentuan layanan</p>
              </div>
            </div>
          </NuxtLink>
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
const openFaq = ref(null)
const isSubmitting = ref(false)
const submitMessage = ref('')
const submitSuccess = ref(false)

const form = ref({
  name: '',
  email: '',
  phone: '',
  category: '',
  message: ''
})

useHead({
  title: 'Support & Help Center - WA Scheduler',
  meta: [
    { name: 'description', content: 'Pusat bantuan WA Scheduler - FAQ, panduan, dan kontak support 24/7' }
  ]
})

const toggleFaq = (index) => {
  openFaq.value = openFaq.value === index ? null : index
}

const handleSubmit = async () => {
  isSubmitting.value = true
  submitMessage.value = ''
  
  try {
    // Simulasi API call - ganti dengan actual API endpoint
    await new Promise(resolve => setTimeout(resolve, 2000))
    
    // Success
    submitSuccess.value = true
    submitMessage.value = '✅ Pesan berhasil dikirim! Tim kami akan segera menghubungi Anda.'
    
    // Reset form
    form.value = {
      name: '',
      email: '',
      phone: '',
      category: '',
      message: ''
    }
    
    // Clear message after 5 seconds
    setTimeout(() => {
      submitMessage.value = ''
    }, 5000)
    
  } catch (error) {
    submitSuccess.value = false
    submitMessage.value = '❌ Terjadi kesalahan. Silakan coba lagi atau hubungi kami via WhatsApp.'
  } finally {
    isSubmitting.value = false
  }
}
</script>

<style scoped>
@keyframes pulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.6; }
}

.animate-pulse {
  animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

select {
  appearance: none;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='none' viewBox='0 0 24 24' stroke='white'%3E%3Cpath stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M19 9l-7 7-7-7'%3E%3C/path%3E%3C/svg%3E");
  background-repeat: no-repeat;
  background-position: right 1rem center;
  background-size: 1.5em 1.5em;
  padding-right: 3rem;
}

select option {
  background-color: #1e293b;
  color: white;
}
</style>