<!-- pages/login.vue -->
<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 flex items-center justify-center p-4">
    <div class="max-w-md w-full">
      <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-8 shadow-2xl">
        <!-- Logo -->
        <div class="text-center mb-8">
          <div class="w-16 h-16 bg-gradient-to-r from-green-400 to-blue-500 rounded-xl flex items-center justify-center mx-auto mb-4">
            <div class="w-10 h-10 bg-white rounded-lg flex items-center justify-center relative">
              <div class="w-6 h-6 grid grid-cols-2 gap-0.5">
                <div class="w-2 h-2 bg-green-500 rounded-sm"></div>
                <div class="w-2 h-2 bg-blue-500 rounded-sm"></div>
                <div class="w-2 h-2 bg-purple-500 rounded-sm"></div>
                <div class="w-2 h-2 bg-green-500 rounded-sm"></div>
              </div>
            </div>
          </div>
          <h1 class="text-2xl font-bold text-white mb-2">WA Scheduler</h1>
          <p class="text-white/70">Cek dengan nomor WhatsApp Anda</p>
        </div>

        <!-- Login Form -->
        <form @submit.prevent="handleLogin" class="space-y-6">
          <div>
            <label class="block text-white mb-2 text-sm font-medium">
              Nomor WhatsApp
            </label>
            <input 
              v-model="phoneNumber"
              type="tel" 
              placeholder="628123456789" 
              class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-xl text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-green-400 transition-all"
              required
            >
            <p class="text-white/50 text-xs mt-1">
              Format: 628xxx (tanpa +, spasi, atau tanda hubung)
            </p>
          </div>

          <button 
            type="submit"
            :disabled="loading || !phoneNumber"
            class="w-full bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 disabled:opacity-50 disabled:cursor-not-allowed text-white font-semibold py-3 rounded-xl transition-all transform hover:scale-105 shadow-lg"
          >
            <span v-if="loading" class="flex items-center justify-center">
              <svg class="animate-spin -ml-1 mr-3 h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
              </svg>
              Checking...
            </span>
            <span v-else>
              Masuk
            </span>
          </button>
        </form>

        <!-- Error Message / Info -->
        <div v-if="errorMessage" class="mt-4 p-4 bg-amber-500/20 border border-amber-500/30 rounded-lg">
          <p class="text-amber-200 text-sm text-center mb-3">{{ errorMessage }}</p>
          <a 
            v-if="showWhatsAppButton"
            href="https://wa.me/6288975326743?text=Buatkan%20jadwal%20untuk%20besok%20jam%207%20pagi"
            target="_blank"
            class="block w-full bg-green-500 hover:bg-green-600 text-white font-semibold py-2.5 rounded-lg transition-all text-center"
          >
            Chat WhatsApp Bot
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Phone number input
const phoneNumber = ref('')
const loading = ref(false)
const errorMessage = ref('')
const showWhatsAppButton = ref(false)

// Runtime config
const config = useRuntimeConfig()

// Handle login
const handleLogin = async () => {
  if (!phoneNumber.value) return
  
  loading.value = true
  errorMessage.value = ''
  showWhatsAppButton.value = false
  
  try {
    // Validate phone number format
    const cleanPhone = phoneNumber.value.replace(/\D/g, '')
    if (!cleanPhone.startsWith('62') || cleanPhone.length < 10) {
      throw new Error('Format nomor tidak valid. Gunakan format 628xxx')
    }
    
    // Check if user exists
    const response = await $fetch(`${config.public.apiBase}/api/dashboard/${cleanPhone}`)
    
    if (response.success) {
      // Store phone number in session/localStorage
      localStorage.setItem('wa_scheduler_phone', cleanPhone)
      
      // Redirect to dashboard
      await navigateTo(`/dashboard/${cleanPhone}`)
    }
  } catch (error) {
    console.error('Login error:', error)
    
    // If user not found (404), show WhatsApp contact instruction
    if (error.statusCode === 404 || error.response?.status === 404 || error.status === 404) {
      errorMessage.value = 'Nomor belum terdaftar. Silakan chat bot WhatsApp terlebih dahulu:'
      showWhatsAppButton.value = true
    } else {
      errorMessage.value = error.message || 'Terjadi kesalahan. Silakan coba lagi.'
      showWhatsAppButton.value = false
    }
  } finally {
    loading.value = false
  }
}

// Auto-login if phone number exists in localStorage
onMounted(() => {
  const savedPhone = localStorage.getItem('wa_scheduler_phone')
  if (savedPhone) {
    phoneNumber.value = savedPhone
  }
})
</script>