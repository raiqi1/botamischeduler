<!-- app/app.vue -->
<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 relative overflow-hidden">
    <!-- Background Animated Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute -top-40 -right-40 w-80 h-80 bg-purple-500 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-pulse"></div>
      <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-blue-500 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-pulse animation-delay-2000"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-60 h-60 bg-green-500 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-pulse animation-delay-4000"></div>
    </div>

    <!-- Navigation -->
    <nav class="relative z-20 px-6 py-4">
      <div class="max-w-7xl mx-auto flex items-center justify-between">
        <div class="flex items-center space-x-3">
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
        </div>
        
        <div class="hidden md:flex items-center space-x-8">
          <a href="#features" class="text-white/80 hover:text-white transition-colors">Features</a>
          <a href="#demo" class="text-white/80 hover:text-white transition-colors">
            How It Works
          </a>
          <!-- <a href="#pricing" class="text-white/80 hover:text-white transition-colors">Pricing</a> -->
          <NuxtLink 
            to="/login" 
            class="bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 text-white px-6 py-2 rounded-full transition-all transform hover:scale-105"
          >
            Login
          </NuxtLink>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative z-10 px-6 pt-20 pb-32">
      <div class="max-w-7xl mx-auto">
        <div class="grid lg:grid-cols-2 gap-12 items-center">
          
          <!-- Left: Hero Content -->
          <div class="text-center lg:text-left">
            <div class="inline-flex items-center bg-gradient-to-r from-green-500/10 to-blue-500/10 border border-green-400/20 rounded-full px-4 py-2 mb-6">
              <span class="w-2 h-2 bg-green-400 rounded-full mr-2 animate-pulse"></span>
              <span class="text-green-300 text-sm font-medium">🚀 Now Available</span>
            </div>
            
            <h1 class="text-5xl lg:text-7xl font-bold text-white mb-6 leading-tight">
              Schedule Smart with
              <span class="bg-gradient-to-r from-green-400 via-blue-400 to-purple-400 bg-clip-text text-transparent">
                WhatsApp Bot
              </span>
            </h1>
            
            <p class="text-xl text-white/80 mb-8 max-w-2xl">
              Kelola jadwal, meeting, dan reminder harian Anda langsung dari WhatsApp. 
              Bot pintar yang mengerti cara kita ngobrol sehari-hari!
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
              <NuxtLink 
                to="/login"
                class="bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 text-white px-8 py-4 rounded-2xl font-semibold text-lg transition-all transform hover:scale-105 shadow-2xl"
              >
                🚀 Login / Register
              </NuxtLink>
              <!-- <button class="backdrop-blur-md bg-white/10 hover:bg-white/20 border border-white/20 text-white px-8 py-4 rounded-2xl font-semibold text-lg transition-all">
                📱 Watch Demo
              </button> -->
            </div>
            
            <div class="flex items-center justify-center lg:justify-start space-x-8 mt-12 text-white/60">
              <div class="text-center">
                <div class="text-2xl font-bold text-white">100%</div>
                <div class="text-sm">Bahasa Indonesia</div>
              </div>
              <div class="text-center">
                <div class="text-2xl font-bold text-white">24/7</div>
                <div class="text-sm">Always Online</div>
              </div>
              <div class="text-center">
                <div class="text-2xl font-bold text-white">AI</div>
                <div class="text-sm">Powered</div>
              </div>
            </div>
          </div>
          
          <!-- Right: Live Previews -->
          <div class="flex flex-row max-sm:flex-col space-y-8 justify-center lg:justify-end">
            <!-- Chat Preview -->
            <div class="relative">
              <div class="relative w-full max-w-lg max-sm:w-full mx-auto bg-gradient-to-b from-slate-800 to-slate-900 rounded-3xl p-1 shadow-2xl">
                <div class="w-full h-[500px] bg-gradient-to-b from-slate-900 to-black rounded-3xl overflow-hidden">
                  
                  <!-- Chat Header -->
                  <div class="bg-gradient-to-r from-green-600 to-green-700 p-4 flex items-center space-x-3">
                    <div class="w-12 h-12 rounded-full bg-white/20 flex items-center justify-center relative">
                      <div class="w-8 h-8 bg-white rounded-lg flex items-center justify-center relative">
                        <div class="w-4 h-4 grid grid-cols-2 gap-0.5">
                          <div class="w-1 h-1 bg-green-500 rounded-sm"></div>
                          <div class="w-1 h-1 bg-blue-500 rounded-sm"></div>
                          <div class="w-1 h-1 bg-purple-500 rounded-sm"></div>
                          <div class="w-1 h-1 bg-green-500 rounded-sm"></div>
                        </div>
                        <div class="absolute -bottom-0.5 -right-0.5 w-1.5 h-1.5 bg-white transform rotate-45"></div>
                      </div>
                    </div>
                    <div>
                      <h3 class="text-white font-semibold">WA Scheduler Bot</h3>
                      <div class="flex items-center text-sm text-green-100">
                        <span class="w-2 h-2 bg-green-300 rounded-full mr-2 animate-pulse"></span>
                        online
                      </div>
                    </div>
                  </div>
                  
                  <!-- Chat Messages -->
                  <div class="flex-1 p-4 space-y-3 h-[430px] overflow-y-auto w-[300px] " ref="chatContainer">
                    <div v-for="(message, index) in visibleMessages" :key="index" 
                         :class="message.isUser ? 'flex justify-end' : 'flex justify-start'"
                         class="opacity-0 animate-fadeIn"
                         :style="{ animationDelay: index * 0.2 + 's' }">
                      <div :class="message.isUser 
                        ? 'bg-green-500 text-white rounded-2xl rounded-br-md px-3 py-2 max-w-[80%] shadow-lg' 
                        : message.isSystem 
                          ? 'bg-blue-600 text-white rounded-2xl px-3 py-2 max-w-[80%] shadow-lg border-l-4 border-yellow-400' 
                          : 'bg-slate-700 text-white rounded-2xl rounded-bl-md px-4 py-3 max-w-[85%] shadow-lg'">
                        <div class="text-sm whitespace-pre-line">{{ message.text }}</div>
                        <span class="text-xs opacity-60 block mt-1">{{ message.time }}</span>
                      </div>
                    </div>
                    
                    <!-- Typing Indicator -->
                    <div v-if="isTyping" class="flex justify-start">
                      <div class="bg-slate-700 text-white rounded-2xl rounded-bl-md px-4 py-3 shadow-lg">
                        <div class="flex space-x-1.5 items-center">
                          <div class="w-2 h-2 bg-white/60 rounded-full animate-bounce"></div>
                          <div class="w-2 h-2 bg-white/60 rounded-full animate-bounce" style="animation-delay: 0.1s"></div>
                          <div class="w-2 h-2 bg-white/60 rounded-full animate-bounce" style="animation-delay: 0.2s"></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              
              <!-- Floating Elements -->
              <div class="absolute -top-4 -left-4 w-8 h-8 bg-green-400 rounded-full animate-pulse"></div>
              <div class="absolute -bottom-4 -right-4 w-6 h-6 bg-blue-400 rounded-full animate-pulse animation-delay-1000"></div>
            </div>

            <!-- Calendar Preview -->
            <div class="relative">
              <div class="relative w-full max-w-md mx-auto bg-gradient-to-b from-slate-800 to-slate-900 rounded-2xl p-4 shadow-2xl border border-white/10">
                <!-- Calendar Header -->
                <div class="flex items-center justify-between mb-3">
                  <h3 class="text-white font-bold text-sm">September 2025</h3>
                  <div class="flex space-x-1">
                    <button class="p-1 text-white/70 hover:text-white hover:bg-white/10 rounded">
                      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                      </svg>
                    </button>
                    <button class="p-1 text-white/70 hover:text-white hover:bg-white/10 rounded">
                      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                      </svg>
                    </button>
                  </div>
                </div>

                <!-- Calendar Grid -->
                <div class="space-y-1">
                  <!-- Day Headers -->
                  <div class="grid grid-cols-7 gap-1">
                    <div v-for="day in ['S', 'M', 'T', 'W', 'T', 'F', 'S']" 
                         :key="day" 
                         class="text-center text-white/50 font-medium text-xs py-1">
                      {{ day }}
                    </div>
                  </div>

                  <!-- Calendar Days -->
                  <div class="grid grid-cols-7 gap-1">
                    <div v-for="day in calendarDays" 
                         :key="day.number"
                         :class="[
                           'aspect-square flex flex-col items-center justify-center rounded-lg text-xs',
                           day.isCurrentMonth 
                             ? 'bg-white/5 text-white' 
                             : 'bg-transparent text-white/20',
                           day.isToday 
                             ? 'ring-1 ring-green-400 bg-green-500/20' 
                             : '',
                           day.hasEvent 
                             ? 'border border-blue-400/30' 
                             : ''
                         ]">
                      <span :class="day.isToday ? 'font-bold text-green-400' : ''">
                        {{ day.number }}
                      </span>
                      <div v-if="day.hasEvent" class="flex space-x-0.5 mt-0.5">
                        <div v-for="i in day.eventCount" :key="i" 
                             :class="[
                               'w-1 h-1 rounded-full',
                               i === 1 ? 'bg-blue-400' : i === 2 ? 'bg-green-400' : 'bg-purple-400'
                             ]">
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- Today's Events -->
                <div class="mt-3 pt-3 border-t border-white/10">
                  <h4 class="text-white/70 text-xs font-medium mb-2">Today's Events</h4>
                  <div class="space-y-1.5">
                    <div class="bg-blue-500/10 border border-blue-400/30 rounded-lg p-2">
                      <div class="text-white text-xs font-medium">Team Meeting</div>
                      <div class="text-white/60 text-xs">14:00 - 15:00</div>
                    </div>
                    <div class="bg-green-500/10 border border-green-400/30 rounded-lg p-2">
                      <div class="text-white text-xs font-medium">Client Call</div>
                      <div class="text-white/60 text-xs">16:00 - 17:00</div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Floating Elements -->
              <div class="absolute -top-3 -right-3 w-6 h-6 bg-purple-400 rounded-full animate-pulse animation-delay-2000"></div>
              <div class="absolute -bottom-3 -left-3 w-5 h-5 bg-pink-400 rounded-full animate-pulse animation-delay-3000"></div>
            </div>
          </div>
          
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="relative z-10 px-6 py-20 bg-black/20">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-4xl lg:text-5xl font-bold text-white mb-6">
            Fitur <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">Unggulan</span>
          </h2>
          <p class="text-xl text-white/80 max-w-3xl mx-auto">
            Semua yang Anda butuhkan untuk mengelola jadwal dengan efisien, langsung dari WhatsApp
          </p>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div class="group backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-green-400 to-teal-400 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <span class="text-2xl">🤖</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-4">Ngobrol Santai Aja</h3>
            <p class="text-white/70">Bicara dengan bot-AI seperti bicara dengan teman. Tidak perlu perintah ribet!</p>
          </div>
          
          <div class="group backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-blue-400 to-purple-400 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <span class="text-2xl">⏰</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-4">Smart Reminders</h3>
            <p class="text-white/70">Pengingat otomatis 30 menit sebelum meeting. Tidak akan terlewat lagi!</p>
          </div>
          
          <div class="group backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-purple-400 to-pink-400 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <span class="text-2xl">📱</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-4">WhatsApp Integration</h3>
            <p class="text-white/70">Langsung terintegrasi dengan WhatsApp yang sudah Anda gunakan sehari-hari.</p>
          </div>
          
          <div class="group backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-orange-400 to-red-400 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <span class="text-2xl">🌟</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-4">Daily Motivation</h3>
            <p class="text-white/70">Dapatkan motivasi harian yang disesuaikan dengan jadwal dan mood Anda.</p>
          </div>
          
          <div class="group backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-teal-400 to-green-400 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <span class="text-2xl">🔄</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-4">Real-time Sync</h3>
            <p class="text-white/70">Semua perubahan jadwal tersinkron secara real-time di semua device.</p>
          </div>
          
          <div class="group backdrop-blur-md bg-white/5 hover:bg-white/10 border border-white/10 rounded-2xl p-8 transition-all hover:-translate-y-2">
            <div class="w-16 h-16 bg-gradient-to-r from-indigo-400 to-purple-400 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <span class="text-2xl">🛡️</span>
            </div>
            <h3 class="text-xl font-bold text-white mb-4">Secure & Private</h3>
            <p class="text-white/70">End-to-end encryption dan privacy yang terjamin untuk semua data Anda.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Demo Section -->
    <section id="demo" class="relative z-10 px-6 py-20">
      <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-4xl lg:text-5xl font-bold text-white mb-6">
          Lihat <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">Cara Kerja</span>
        </h2>
        <p class="text-xl text-white/80 mb-12">
          Sederhana, cepat, dan powerful. Cukup chat seperti biasa!
        </p>
        
        <div class="backdrop-blur-md bg-white/10 border border-white/20 rounded-3xl p-8">
          <div class="grid md:grid-cols-3 gap-8">
            <div class="text-center">
              <div class="w-20 h-20 bg-gradient-to-r from-green-400 to-teal-400 rounded-full flex items-center justify-center mx-auto mb-4">
                <span class="text-3xl">💬</span>
              </div>
              <h3 class="text-lg font-bold text-white mb-2">1. Chat Normal</h3>
              <p class="text-white/70 text-sm">Kirim pesan seperti "buat meeting besok jam 2"</p>
            </div>
            
            <div class="text-center">
              <div class="w-20 h-20 bg-gradient-to-r from-blue-400 to-purple-400 rounded-full flex items-center justify-center mx-auto mb-4">
                <span class="text-3xl">🧠</span>
              </div>
              <h3 class="text-lg font-bold text-white mb-2">2. AI Processes</h3>
              <p class="text-white/70 text-sm">Bot memahami dan memproses permintaan Anda</p>
            </div>
            
            <div class="text-center">
              <div class="w-20 h-20 bg-gradient-to-r from-purple-400 to-pink-400 rounded-full flex items-center justify-center mx-auto mb-4">
                <span class="text-3xl">✅</span>
              </div>
              <h3 class="text-lg font-bold text-white mb-2">3. Done!</h3>
              <p class="text-white/70 text-sm">Jadwal dibuat dan reminder diatur otomatis</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="relative z-10 px-6 py-20">
      <div class="max-w-4xl mx-auto text-center">
        <div class="backdrop-blur-md bg-gradient-to-r from-green-500/20 to-blue-500/20 border border-green-400/30 rounded-3xl p-12">
          <h2 class="text-4xl lg:text-5xl font-bold text-white mb-6">
            Siap Mulai Mengatur Jadwal?
          </h2>
          <p class="text-xl text-white/80 mb-8">
            Join ribuan pengguna yang sudah merasakan kemudahan mengatur jadwal dengan AI
          </p>
          
          <div class="flex flex-col sm:flex-row gap-4 justify-center mb-8">
            <NuxtLink 
              to="/login"
              class="bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 text-white px-10 py-4 rounded-2xl font-bold text-lg transition-all transform hover:scale-105 shadow-2xl"
            >
              🚀 Login / Register 
            </NuxtLink>
            <NuxtLink 
              to="/support"
              class="bg-white/10 hover:bg-white/20 text-white px-10 py-4 rounded-2xl font-bold text-lg transition-all transform hover:scale-105 shadow-2xl"
            >
              ❓ Bantuan
            </NuxtLink>
          </div>
          
          <p class="text-white/60 text-sm">
            ✨ Gratis  • 🚫 No Credit Card Required • ⚡ Setup dalam 2 menit
          </p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="relative z-10 px-6 py-12 border-t border-white/10">
      <div class="max-w-7xl mx-auto">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="flex items-center space-x-3 mb-4 md:mb-0">
            <div class="w-8 h-8 bg-gradient-to-r from-green-400 to-blue-500 rounded-lg flex items-center justify-center relative">
              <div class="w-5 h-5 bg-white rounded-md flex items-center justify-center">
                <div class="w-3 h-3 grid grid-cols-2 gap-0.5">
                  <div class="w-0.5 h-0.5 bg-green-500 rounded-sm"></div>
                  <div class="w-0.5 h-0.5 bg-blue-500 rounded-sm"></div>
                  <div class="w-0.5 h-0.5 bg-purple-500 rounded-sm"></div>
                  <div class="w-0.5 h-0.5 bg-green-500 rounded-sm"></div>
                </div>
              </div>
              <div class="absolute -bottom-0.5 -right-0.5 w-1.5 h-1.5 bg-white transform rotate-45"></div>
            </div>
            <span class="text-lg font-bold text-white">WA Scheduler</span>
          </div>
          
          <div class="flex items-center space-x-6 text-white/60">
            <NuxtLink to="/privacy" class="hover:text-white transition-colors">Privacy</NuxtLink>
            <NuxtLink to="/terms" class="hover:text-white transition-colors">Terms</NuxtLink>
            <NuxtLink to="/support" class="hover:text-white transition-colors">Support</NuxtLink>
            <span>© 2025 WA Scheduler. All rights reserved.</span>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
const isTyping = ref(false)
const chatContainer = ref(null)
const visibleMessages = ref([])

// Sample messages for demo - LENGKAP!
const demoMessages = [
  { text: 'bikin meeting besok jam 2 siang', isUser: true, time: '14:30' },
  { 
    text: '✅ Event Berhasil Dibuat!\n📋 Judul: Meeting\n📅 Tanggal: Senin, 29 Sep 2025\n🕐 Waktu: 14.00\n🔔 Pengingat: 30 menit sebelumnya\n🆔 Event ID: 21', 
    isUser: false, 
    time: '14:31' 
  },
  { text: 'jadwal minggu depan ada apa aja?', isUser: true, time: '14:32' },
  { 
    text: '📅 Jadwal Minggu Depan (30 Sep - 6 Okt)\n📍 Senin:\n• Meeting Client - 14.00\n• Review Project - 16.00\n📍 Rabu:\n• Presentasi Tim - 10.00\n📍 Jumat:\n• Training Karyawan - 09.00\n📍 Sabtu:\n• Event Launching - 19.00', 
    isUser: false, 
    time: '14:32' 
  },
  { text: 'kirim motivasi setiap hari jam 7 pagi', isUser: true, time: '14:33' },
  { 
    text: '🌟 MOTIVASI HARIAN DIAKTIFKAN! 🌟\n⏰ Waktu: Setiap hari jam 07:00 WIB\n📝 Jenis: Motivasi inspiratif harian\n🤖 AI Generated: Konten fresh setiap hari\n✅ Mulai besok pagi, Anda akan menerima motivasi harian!\n💡 Tips:\n• Reply "motivasi stop" untuk menghentikan\n• Reply "motivasi ubah jam 8" untuk ubah waktu', 
    isUser: false, 
    time: '14:33' 
  },
  // MOTIVASI HARIAN MESSAGE
  { 
    text: '🌟 MOTIVASI HARIAN 🌟\n*Selamat pagi! 🌞*\nHari ini adalah kanvas kosong yang menunggu goresan terbaikmu. Jangan hanya melewati waktu—hidupilah setiap momen dengan semangat dan rasa syukur.\nLakukan satu hal kecil hari ini yang membuatmu bangga, sekecil apa pun. Ingat, langkah kecil tetap membawamu maju. 🚀\nKamu punya kekuatan untuk menjadikan hari ini berarti. Yakini, lalu wujudkan! 💪\nSemangat pagi! ✨\n⏰ 07.00 WIB\n💡 Semoga harimu amazing!\n─────────────────\n💬 Reply "motivasi stop" untuk berhenti\n⚙ Reply "motivasi setting" untuk ubah waktu', 
    isUser: false, 
    time: '07:00', 
    isSystem: true 
  },
  { text: 'ubah waktu motivasi ke jam 6 pagi', isUser: true, time: '14:34' },
  { 
    text: '⏰ WAKTU MOTIVASI DIUBAH!\n✅ Waktu baru: Setiap hari jam 06:00 WIB\n🔄 Perubahan: Berlaku mulai besok\n📱 Status: Aktif\n💡 Motivasi akan dikirim sesuai waktu baru!', 
    isUser: false, 
    time: '14:34' 
  },
  // REMINDER EVENT MESSAGE
  { 
    text: '⏰ REMINDER EVENT ⏰\n📅 Meeting Client akan dimulai dalam 30 menit!\n\n📋 Detail Event:\n• Judul: Meeting Client\n• Tanggal: Senin, 29 Sep 2025\n• Waktu: 14:00 WIB\n• Durasi: 1 jam (estimasi)\n• Lokasi: Video Call Zoom\n\n🎯 Persiapan:\n• Siapkan laptop dan headset\n• Review proposal yang akan dipresentasikan\n• Join link Zoom: meeting.zoom.us/j/123456\n\n⚡ Jangan sampai terlambat!\n💼 Semoga lancar!', 
    isUser: false, 
    time: '13:30', 
    isSystem: true 
  },
  { text: 'edit event meeting jadi jam 3 sore', isUser: true, time: '14:35' },
  { 
    text: '🔍 Pilih Event Meeting:\n1. Meeting Client\n   📅 Senin, 29 Sep\n   🕐 14.00\n2. Meeting Project Review\n   📅 Selasa, 30 Sep\n   🕐 10.00\n💬 Ketik angka pilihan (1, 2, dst)', 
    isUser: false, 
    time: '14:35' 
  },
  { text: '1', isUser: true, time: '14:36' },
  // JADWAL BENTROK DETECTION
  { 
    text: '⚠️ JADWAL BENTROK TERDETEKSI!\n📅 Waktu baru (15:00) bentrok dengan:\n\n🔴 KONFLIK:\n• Review Project\n• Waktu: 15:00-16:30\n• Tanggal: Senin, 29 Sep\n\n💡 SOLUSI:\n1. Geser Meeting Client ke jam 16:45\n2. Geser Review Project ke jam 13:00\n3. Perpendek durasi salah satu meeting\n\n❓ Pilih opsi:\nKetik "1", "2", "3" atau "batal" untuk membatalkan', 
    isUser: false, 
    time: '14:36' 
  },
  { text: 'batal', isUser: true, time: '14:37' },
  { 
    text: '✅ EDIT DIBATALKAN\n📅 Event Meeting Client tetap pada:\n• Tanggal: Senin, 29 Sep 2025\n• Waktu: 14:00 WIB\n\n💡 Tips: Cek jadwal dengan "lihat jadwal hari ini" sebelum edit untuk menghindari bentrok', 
    isUser: false, 
    time: '14:37' 
  },
  { text: 'jadwal hari rabu', isUser: true, time: '14:38' },
  { 
    text: '📅 Jadwal Hari Rabu (2 Okt)\n1. Morning Stand-up\n   📅 Rabu, 2 Okt\n   🕐 09.00\n2. Presentasi Tim\n   📅 Rabu, 2 Okt\n   🕐 10.00\n3. Lunch Meeting\n   📅 Rabu, 2 Okt\n   🕐 12.00\n4. Code Review Session\n   📅 Rabu, 2 Okt\n   🕐 15.00', 
    isUser: false, 
    time: '14:38' 
  },
  { text: 'stop motivasi harian', isUser: true, time: '14:39' },
  { 
    text: '🛑 MOTIVASI HARIAN DIHENTIKAN\n✅ Motivasi harian berhasil dinonaktifkan\n📵 Anda tidak akan menerima motivasi otomatis lagi\n💡 Untuk mengaktifkan kembali:\n"kirim motivasi setiap hari jam 7 pagi"', 
    isUser: false, 
    time: '14:39' 
  }
]


// Calendar data
const calendarDays = ref([
  { number: 1, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 2, isCurrentMonth: true, hasEvent: true, eventCount: 1 },
  { number: 3, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 4, isCurrentMonth: true, hasEvent: true, eventCount: 2 },
  { number: 5, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 6, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 7, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 8, isCurrentMonth: true, hasEvent: true, eventCount: 1 },
  { number: 9, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 10, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 11, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 12, isCurrentMonth: true, hasEvent: true, eventCount: 1 },
  { number: 13, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 14, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 15, isCurrentMonth: true, hasEvent: true, eventCount: 3 },
  { number: 16, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 17, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 18, isCurrentMonth: true, hasEvent: true, eventCount: 1 },
  { number: 19, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 20, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 21, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 22, isCurrentMonth: true, hasEvent: true, eventCount: 2 },
  { number: 23, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 24, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 25, isCurrentMonth: true, hasEvent: true, eventCount: 1 },
  { number: 26, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 27, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 28, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 29, isCurrentMonth: true, hasEvent: false, eventCount: 0 },
  { number: 30, isCurrentMonth: true, hasEvent: true, eventCount: 2, isToday: true },
])

// Auto demo conversation
onMounted(() => {
  setTimeout(() => {
    startDemoConversation()
  }, 1500)
})

const startDemoConversation = async () => {
  for (let i = 0; i < demoMessages.length; i++) {
    if (i % 2 === 1) {
      isTyping.value = true
      await new Promise(resolve => setTimeout(resolve, 800))
      isTyping.value = false
    }
    
    visibleMessages.value.push(demoMessages[i])
    scrollToBottom()
    
    await new Promise(resolve => setTimeout(resolve, i % 2 === 0 ? 1000 : 2500))
  }
  
  setTimeout(() => {
    visibleMessages.value = []
    startDemoConversation()
  }, 4000)
}

const scrollToBottom = () => {
  nextTick(() => {
    if (chatContainer.value) {
      chatContainer.value.scrollTop = chatContainer.value.scrollHeight
    }
  })
}
</script>

<style>
@keyframes pulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.6; }
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes bounce {
  0%, 80%, 100% {
    transform: scale(0);
  }
  40% {
    transform: scale(1);
  }
}

.animate-fadeIn {
  animation: fadeIn 0.6s ease-out forwards;
}

.animate-bounce {
  animation: bounce 1.4s infinite ease-in-out both;
}

.animation-delay-1000 {
  animation-delay: 1s;
}

.animation-delay-2000 {
  animation-delay: 2s;
}

.animation-delay-3000 {
  animation-delay: 3s;
}

.animation-delay-4000 {
  animation-delay: 4s;
}

::-webkit-scrollbar {
  width: 3px;
}

::-webkit-scrollbar-track {
  background: rgba(255, 255, 255, 0.1);
}

::-webkit-scrollbar-thumb {
  background: rgba(255, 255, 255, 0.3);
  border-radius: 2px;
}

html {
  scroll-behavior: smooth;
}
</style>