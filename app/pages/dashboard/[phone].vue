<!-- pages/dashboard/[phone].vue -->
<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900">
    <!-- Mobile Navigation -->
    <nav class="border-b border-white/10 bg-black/20 backdrop-blur-md">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <!-- Logo -->
          <div class="flex items-center space-x-2 sm:space-x-3">
            <div class="w-8 h-8 sm:w-10 sm:h-10 bg-gradient-to-r from-green-400 to-blue-500 rounded-xl flex items-center justify-center">
              <div class="w-4 h-4 sm:w-6 sm:h-6 bg-white rounded-lg flex items-center justify-center">
                <div class="w-3 h-3 sm:w-4 sm:h-4 grid grid-cols-2 gap-0.5">
                  <div class="w-0.5 h-0.5 sm:w-1 sm:h-1 bg-green-500 rounded-sm"></div>
                  <div class="w-0.5 h-0.5 sm:w-1 sm:h-1 bg-blue-500 rounded-sm"></div>
                  <div class="w-0.5 h-0.5 sm:w-1 sm:h-1 bg-purple-500 rounded-sm"></div>
                  <div class="w-0.5 h-0.5 sm:w-1 sm:h-1 bg-green-500 rounded-sm"></div>
                </div>
              </div>
            </div>
            <div>
              <h1 class="text-sm sm:text-lg font-bold text-white">WA Scheduler</h1>
              <p class="text-xs text-white/60 hidden sm:block">{{ phoneNumber }}</p>
            </div>
          </div>

          <!-- Actions -->
          <div class="flex items-center space-x-2 sm:space-x-4">
            <button 
              @click="refreshData"
              class="p-2 text-white/70 hover:text-white hover:bg-white/10 rounded-lg transition-all"
            >
              <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"></path>
              </svg>
            </button>
            
            <button 
              @click="logout"
              class="px-3 py-2 sm:px-4 sm:py-2 bg-red-500/20 hover:bg-red-500/30 text-red-300 rounded-lg transition-all text-xs sm:text-sm"
            >
              Logout
            </button>
          </div>
        </div>
      </div>
    </nav>

    <!-- Loading State -->
    <div v-if="loading" class="flex items-center justify-center min-h-[400px]">
      <div class="text-center text-white">
        <svg class="animate-spin mx-auto h-12 w-12 text-green-400 mb-4" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
          <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
          <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
        </svg>
        <p class="text-sm">Memuat data dashboard...</p>
      </div>
    </div>

    <!-- Dashboard Content -->
    <div v-else-if="dashboardData" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 sm:py-8">
      <!-- Mobile Stats Cards -->
      <div class="grid grid-cols-2 lg:grid-cols-4 gap-3 sm:gap-6 mb-6 sm:mb-8">
        <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-3 sm:p-6">
          <div class="flex items-center lg:flex-col lg:items-start lg:space-y-2">
            <div class="p-2 sm:p-3 rounded-full bg-blue-500/20 mr-3 lg:mr-0">
              <svg class="w-4 h-4 sm:w-6 sm:h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xs sm:text-sm text-white/70">Events</p>
              <p class="text-lg sm:text-2xl font-bold text-white">{{ dashboardData.stats.totalEvents }}</p>
            </div>
          </div>
        </div>

        <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-3 sm:p-6">
          <div class="flex items-center lg:flex-col lg:items-start lg:space-y-2">
            <div class="p-2 sm:p-3 rounded-full bg-yellow-500/20 mr-3 lg:mr-0">
              <svg class="w-4 h-4 sm:w-6 sm:h-6 text-yellow-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xs sm:text-sm text-white/70">Reminders</p>
              <p class="text-lg sm:text-2xl font-bold text-white">{{ dashboardData.stats.activeReminders }}</p>
            </div>
          </div>
        </div>

        <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-3 sm:p-6">
          <div class="flex items-center lg:flex-col lg:items-start lg:space-y-2">
            <div class="p-2 sm:p-3 rounded-full bg-green-500/20 mr-3 lg:mr-0">
              <svg class="w-4 h-4 sm:w-6 sm:h-6 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xs sm:text-sm text-white/70">Today</p>
              <p class="text-lg sm:text-2xl font-bold text-white">{{ dashboardData.todayEvents.length }}</p>
            </div>
          </div>
        </div>

        <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-3 sm:p-6">
          <div class="flex items-center lg:flex-col lg:items-start lg:space-y-2">
            <div class="p-2 sm:p-3 rounded-full bg-purple-500/20 mr-3 lg:mr-0">
              <svg class="w-4 h-4 sm:w-6 sm:h-6 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xs sm:text-sm text-white/70">Motivation</p>
              <p class="text-sm sm:text-xl lg:text-2xl font-bold text-white">{{ dashboardData.motivationSettings ? 'ON' : 'OFF' }}</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Mobile Layout: Stack vertically -->
      <div class="space-y-6 lg:grid lg:grid-cols-4 lg:gap-8 lg:space-y-0">
        <!-- Calendar View -->
        <div class="lg:col-span-3">
          <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-4 sm:p-6">
            <!-- Calendar Header -->
            <div class="flex items-center justify-between mb-4 sm:mb-6">
              <div class="flex items-center space-x-2">
                <button 
                  @click="previousMonth"
                  class="p-2 text-white/70 hover:text-white hover:bg-white/10 rounded-lg transition-all"
                >
                  <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                  </svg>
                </button>
                <h3 class="text-sm sm:text-lg font-semibold text-white min-w-[140px] sm:min-w-[200px] text-center">
                  {{ formatMonthYear(currentMonth) }}
                </h3>
                <button 
                  @click="nextMonth"
                  class="p-2 text-white/70 hover:text-white hover:bg-white/10 rounded-lg transition-all"
                >
                  <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                  </svg>
                </button>
              </div>
              <button 
                @click="showCreateEventModal = true"
                class="px-3 py-2 sm:px-4 sm:py-2 bg-green-500 hover:bg-green-600 text-white rounded-lg text-xs sm:text-sm font-medium transition-all"
              >
                + Event
              </button>
            </div>

            <!-- Mobile Calendar Grid -->
            <div class="calendar-grid">
              <!-- Day Headers -->
              <div class="grid grid-cols-7 gap-1 mb-2">
                <div v-for="day in ['M', 'S', 'S', 'R', 'K', 'J', 'S']" 
                     :key="day" 
                     class="text-center text-white/70 font-medium py-1 sm:py-2 text-xs sm:text-sm">
                  {{ day }}
                </div>
              </div>

              <!-- Calendar Days -->
              <div class="grid grid-cols-7 gap-1">
                <div v-for="day in calendarDays" 
                     :key="day.key"
                     :class="[
                       'min-h-[60px] sm:min-h-[80px] lg:min-h-[100px] p-1 sm:p-2 rounded-lg border transition-all cursor-pointer',
                       day.isCurrentMonth 
                         ? 'bg-white/5 border-white/10 hover:bg-white/10' 
                         : 'bg-white/2 border-white/5',
                       day.isToday 
                         ? 'ring-1 sm:ring-2 ring-green-400/50 bg-green-500/10' 
                         : '',
                       day.hasEvents 
                         ? 'border-blue-400/30' 
                         : ''
                     ]"
                     @click="selectDate(day.date)">
                  <!-- Day Number -->
                  <div :class="[
                    'text-xs sm:text-sm font-medium mb-1',
                    day.isCurrentMonth ? 'text-white' : 'text-white/30',
                    day.isToday ? 'text-green-400 font-bold' : ''
                  ]">
                    {{ day.date.getDate() }}
                  </div>

                  <!-- Mobile Events (dots only) -->
                  <div v-if="day.events.length > 0" class="space-y-0.5">
                    <!-- Show max 1 event on mobile, 2 on larger screens -->
                    <div v-for="event in day.events.slice(0, isMobile ? 1 : 2)" 
                         :key="event.id"
                         :class="[
                           'text-xs px-1 py-0.5 sm:px-2 sm:py-1 rounded truncate',
                           getEventColor(event)
                         ]"
                         :title="event.summary + ' - ' + formatTime(event.startDatetime)">
                      <span class="hidden sm:inline">{{ event.summary }}</span>
                      <span class="sm:hidden w-2 h-2 rounded-full inline-block bg-current"></span>
                    </div>
                    <div v-if="day.events.length > (isMobile ? 1 : 2)" 
                         class="text-xs text-white/50 px-1 sm:px-2">
                      <span class="hidden sm:inline">+{{ day.events.length - 2 }} lainnya</span>
                      <span class="sm:hidden text-xs">+{{ day.events.length - 1 }}</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Sidebar -->
        <div class="space-y-4 sm:space-y-6">
          <!-- Selected Date Events -->
          <div v-if="selectedDate" class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-4 sm:p-6">
            <h3 class="text-base sm:text-lg font-bold text-white mb-4">
              {{ formatSelectedDate(selectedDate) }}
            </h3>
            
            <div v-if="selectedDateEvents.length === 0" class="text-center py-4">
              <p class="text-white/50 text-sm">Tidak ada event</p>
            </div>
            
            <div v-else class="space-y-3">
              <div v-for="event in selectedDateEvents" 
                   :key="event.id"
                   class="bg-white/5 rounded-lg p-3 hover:bg-white/10 transition-all group">
                <div class="flex items-start justify-between">
                  <div class="flex-1">
                    <h4 class="text-white text-sm font-medium">{{ event.summary }}</h4>
                    <p class="text-white/60 text-xs">
                      {{ formatTime(event.startDatetime) }}
                      <span v-if="event.endDatetime">
                        - {{ formatTime(event.endDatetime) }}
                      </span>
                    </p>
                  </div>
                  <button 
                    @click="deleteEvent(event.id)"
                    class="opacity-0 group-hover:opacity-100 p-1 text-red-400 hover:text-red-300 hover:bg-red-500/20 rounded transition-all"
                  >
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
                    </svg>
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- Motivation Settings -->
          <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-4 sm:p-6">
            <h3 class="text-base sm:text-lg font-bold text-white mb-4">Motivasi Harian</h3>
            
            <div v-if="dashboardData.motivationSettings" class="space-y-4">
              <div class="flex items-center justify-between">
                <span class="text-white/70 text-sm">Status</span>
                <span class="px-3 py-1 bg-green-500/20 text-green-300 rounded-full text-xs sm:text-sm">Active</span>
              </div>
              <div class="flex items-center justify-between">
                <span class="text-white/70 text-sm">Waktu</span>
                <span class="text-white text-sm">{{ dashboardData.motivationSettings.time }}</span>
              </div>
              <button 
                @click="toggleMotivation(false)"
                class="w-full px-4 py-2 bg-red-500/20 hover:bg-red-500/30 text-red-300 rounded-lg transition-all text-sm"
              >
                Matikan
              </button>
            </div>
            
            <div v-else class="text-center">
              <p class="text-white/50 mb-4 text-sm">Motivasi harian tidak aktif</p>
              <button 
                @click="showMotivationModal = true"
                class="w-full px-4 py-2 bg-green-500 hover:bg-green-600 text-white rounded-lg transition-all text-sm"
              >
                Aktifkan
              </button>
            </div>
          </div>

          <!-- Quick Stats - Hidden on mobile to save space -->
          <div class="hidden sm:block bg-white/10 backdrop-blur-md border border-white/20 rounded-xl sm:rounded-2xl p-4 sm:p-6">
            <h3 class="text-base sm:text-lg font-bold text-white mb-4">This Month</h3>
            
            <div class="space-y-3">
              <div class="flex justify-between items-center">
                <span class="text-white/70 text-sm">Total Events</span>
                <span class="text-white font-medium">{{ currentMonthEvents.length }}</span>
              </div>
              <div class="flex justify-between items-center">
                <span class="text-white/70 text-sm">This Week</span>
                <span class="text-white font-medium">{{ thisWeekEvents.length }}</span>
              </div>
              <div class="flex justify-between items-center">
                <span class="text-white/70 text-sm">Remaining</span>
                <span class="text-white font-medium">{{ upcomingEvents.length }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Error State -->
    <div v-else-if="error" class="flex items-center justify-center min-h-[400px] px-4">
      <div class="text-center text-white">
        <svg class="w-12 h-12 text-red-400 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
        <p class="mb-4 text-sm">{{ error }}</p>
        <button 
          @click="loadDashboardData"
          class="px-4 py-2 bg-green-500 hover:bg-green-600 text-white rounded-lg transition-all"
        >
          Coba Lagi
        </button>
      </div>
    </div>

    <!-- Mobile-Optimized Create Event Modal -->
    <div v-if="showCreateEventModal" class="fixed inset-0 bg-black/50 flex items-center justify-center p-4 z-50">
      <div class="bg-slate-800 rounded-2xl p-6 w-full max-w-md border border-white/20 max-h-[90vh] overflow-y-auto">
        <h3 class="text-xl font-bold text-white mb-4">Buat Event Baru</h3>
        
        <form @submit.prevent="createEvent" class="space-y-4">
          <div>
            <label class="block text-white/70 text-sm mb-2">Judul Event</label>
            <input 
              v-model="newEvent.summary"
              type="text" 
              class="w-full px-3 py-2 bg-white/10 border border-white/20 rounded-lg text-white placeholder-white/50 text-base"
              placeholder="Meeting dengan klien"
              required
            >
          </div>
          
          <div>
            <label class="block text-white/70 text-sm mb-2">Tanggal & Waktu</label>
            <input 
              v-model="newEvent.datetime"
              type="datetime-local" 
              class="w-full px-3 py-2 bg-white/10 border border-white/20 rounded-lg text-white text-base"
              required
            >
          </div>
          
          <div class="flex space-x-3 pt-4">
            <button 
              type="button"
              @click="showCreateEventModal = false"
              class="flex-1 px-4 py-2 bg-white/10 hover:bg-white/20 text-white rounded-lg transition-all"
            >
              Batal
            </button>
            <button 
              type="submit"
              :disabled="creatingEvent"
              class="flex-1 px-4 py-2 bg-green-500 hover:bg-green-600 disabled:opacity-50 text-white rounded-lg transition-all"
            >
              {{ creatingEvent ? 'Creating...' : 'Buat Event' }}
            </button>
          </div>
        </form>
      </div>
    </div>

    <!-- Mobile-Optimized Motivation Setup Modal -->
    <div v-if="showMotivationModal" class="fixed inset-0 bg-black/50 flex items-center justify-center p-4 z-50">
      <div class="bg-slate-800 rounded-2xl p-6 w-full max-w-md border border-white/20 max-h-[90vh] overflow-y-auto">
        <h3 class="text-xl font-bold text-white mb-4">Setup Motivasi Harian</h3>
        
        <form @submit.prevent="setupMotivation" class="space-y-4">
          <div>
            <label class="block text-white/70 text-sm mb-2">Waktu Pengiriman</label>
            <input 
              v-model="motivationTime"
              type="time" 
              class="w-full px-3 py-2 bg-white/10 border border-white/20 rounded-lg text-white text-base"
              required
            >
            <p class="text-white/50 text-xs mt-1">Motivasi akan dikirim setiap hari pada waktu ini</p>
          </div>
          
          <div class="flex space-x-3 pt-4">
            <button 
              type="button"
              @click="showMotivationModal = false"
              class="flex-1 px-4 py-2 bg-white/10 hover:bg-white/20 text-white rounded-lg transition-all"
            >
              Batal
            </button>
            <button 
              type="submit"
              :disabled="settingMotivation"
              class="flex-1 px-4 py-2 bg-green-500 hover:bg-green-600 disabled:opacity-50 text-white rounded-lg transition-all"
            >
              {{ settingMotivation ? 'Setting...' : 'Aktifkan' }}
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, watch } from 'vue'

// Route params
const route = useRoute()
const phoneNumber = route.params.phone

// Runtime config
const config = useRuntimeConfig()

// Mobile detection
const isMobile = ref(false)

// State
const dashboardData = ref(null)
const loading = ref(true)
const error = ref('')
const currentMonth = ref(new Date())
const selectedDate = ref(new Date())

// Modals
const showCreateEventModal = ref(false)
const showMotivationModal = ref(false)

// Forms
const newEvent = ref({
  summary: '',
  datetime: ''
})
const motivationTime = ref('07:00')

// Loading states
const creatingEvent = ref(false)
const settingMotivation = ref(false)

// Calendar computeds
const calendarDays = computed(() => {
  const year = currentMonth.value.getFullYear()
  const month = currentMonth.value.getMonth()
  
  const firstDayOfMonth = new Date(year, month, 1)
  const lastDayOfMonth = new Date(year, month + 1, 0)
  
  // Adjust for Monday start (Monday = 1, Sunday = 0)
  const startDate = new Date(firstDayOfMonth)
  const firstDayOfWeek = firstDayOfMonth.getDay()
  const mondayOffset = firstDayOfWeek === 0 ? 6 : firstDayOfWeek - 1
  startDate.setDate(startDate.getDate() - mondayOffset)
  
  // Get last day to show
  const endDate = new Date(lastDayOfMonth)
  const lastDayOfWeek = lastDayOfMonth.getDay()
  const sundayOffset = lastDayOfWeek === 0 ? 0 : 7 - lastDayOfWeek
  endDate.setDate(endDate.getDate() + sundayOffset)
  
  const days = []
  const currentDate = new Date(startDate)
  
  while (currentDate <= endDate) {
    const dayEvents = getEventsForDate(currentDate)
    const today = new Date()
    
    days.push({
      key: currentDate.getTime(),
      date: new Date(currentDate),
      isCurrentMonth: currentDate.getMonth() === month,
      isToday: currentDate.toDateString() === today.toDateString(),
      events: dayEvents,
      hasEvents: dayEvents.length > 0
    })
    
    currentDate.setDate(currentDate.getDate() + 1)
  }
  
  return days
})

const selectedDateEvents = computed(() => {
  if (!selectedDate.value) return []
  return getEventsForDate(selectedDate.value)
})

const currentMonthEvents = computed(() => {
  if (!dashboardData.value) return []
  
  const year = currentMonth.value.getFullYear()
  const month = currentMonth.value.getMonth()
  
  return dashboardData.value.upcomingEvents.filter(event => {
    const eventDate = new Date(event.startDatetime)
    return eventDate.getFullYear() === year && eventDate.getMonth() === month
  })
})

const thisWeekEvents = computed(() => {
  if (!dashboardData.value) return []
  
  const now = new Date()
  const startOfWeek = new Date(now)
  const dayOfWeek = now.getDay()
  const mondayOffset = dayOfWeek === 0 ? 6 : dayOfWeek - 1
  startOfWeek.setDate(now.getDate() - mondayOffset)
  startOfWeek.setHours(0, 0, 0, 0)
  
  const endOfWeek = new Date(startOfWeek)
  endOfWeek.setDate(startOfWeek.getDate() + 6)
  endOfWeek.setHours(23, 59, 59, 999)
  
  return dashboardData.value.upcomingEvents.filter(event => {
    const eventDate = new Date(event.startDatetime)
    return eventDate >= startOfWeek && eventDate <= endOfWeek
  })
})

const upcomingEvents = computed(() => {
  if (!dashboardData.value) return []
  
  const now = new Date()
  return dashboardData.value.upcomingEvents.filter(event => {
    const eventDate = new Date(event.startDatetime)
    return eventDate > now
  })
})

// Methods
const checkIfMobile = () => {
  isMobile.value = window.innerWidth < 640
}

const getEventsForDate = (date) => {
  if (!dashboardData.value) return []
  
  const targetDate = date.toDateString()
  
  // Combine all events
  const allEvents = [
    ...(dashboardData.value.todayEvents || []),
    ...(dashboardData.value.upcomingEvents || []),
    ...(dashboardData.value.recentEvents || [])
  ]
  
  // Remove duplicates and filter by date
  const uniqueEvents = allEvents.filter((event, index, self) => 
    index === self.findIndex(e => e.id === event.id) &&
    new Date(event.startDatetime).toDateString() === targetDate
  )
  
  return uniqueEvents.sort((a, b) => new Date(a.startDatetime) - new Date(b.startDatetime))
}

const getEventColor = (event) => {
  const colors = [
    'bg-blue-500/20 text-blue-300 border border-blue-500/30',
    'bg-green-500/20 text-green-300 border border-green-500/30',
    'bg-purple-500/20 text-purple-300 border border-purple-500/30',
    'bg-orange-500/20 text-orange-300 border border-orange-500/30',
    'bg-pink-500/20 text-pink-300 border border-pink-500/30'
  ]
  
  // Simple hash function to consistently assign colors
  const hash = event.summary.split('').reduce((a, b) => {
    a = ((a << 5) - a) + b.charCodeAt(0)
    return a & a
  }, 0)
  
  return colors[Math.abs(hash) % colors.length]
}

const previousMonth = () => {
  currentMonth.value = new Date(currentMonth.value.getFullYear(), currentMonth.value.getMonth() - 1, 1)
}

const nextMonth = () => {
  currentMonth.value = new Date(currentMonth.value.getFullYear(), currentMonth.value.getMonth() + 1, 1)
}

const selectDate = (date) => {
  selectedDate.value = new Date(date)
}

const formatMonthYear = (date) => {
  return date.toLocaleDateString('id-ID', { 
    month: 'long', 
    year: 'numeric' 
  })
}

const formatSelectedDate = (date) => {
  const options = isMobile.value 
    ? { weekday: 'short', day: 'numeric', month: 'short' }
    : { weekday: 'long', day: 'numeric', month: 'long', year: 'numeric' }
  
  return date.toLocaleDateString('id-ID', options)
}

const formatTime = (datetime) => {
  return new Date(datetime).toLocaleTimeString('id-ID', {
    hour: '2-digit',
    minute: '2-digit'
  })
}

// Load dashboard data
const loadDashboardData = async () => {
  loading.value = true
  error.value = ''
  
  try {
    const response = await $fetch(`${config.public.apiBase}/api/dashboard/${phoneNumber}`)
    
    if (response.success) {
      dashboardData.value = response.data
    } else {
      error.value = response.message || 'Gagal memuat data'
    }
  } catch (err) {
    console.error('Dashboard load error:', err)
    error.value = 'User tidak ditemukan atau belum pernah menggunakan bot WhatsApp'
  } finally {
    loading.value = false
  }
}

// Create new event
const createEvent = async () => {
  if (!newEvent.value.summary || !newEvent.value.datetime) return
  
  creatingEvent.value = true
  
  try {
    const response = await $fetch(`${config.public.apiBase}/api/events`, {
      method: 'POST',
      body: {
        phoneNumber,
        summary: newEvent.value.summary,
        startDateTime: new Date(newEvent.value.datetime).toISOString()
      }
    })
    
    if (response.success) {
      showCreateEventModal.value = false
      newEvent.value = { summary: '', datetime: '' }
      await loadDashboardData() // Refresh data
    } else {
      alert(response.message || 'Gagal membuat event')
    }
  } catch (err) {
    console.error('Create event error:', err)
    alert('Gagal membuat event')
  } finally {
    creatingEvent.value = false
  }
}

// Delete event
const deleteEvent = async (eventId) => {
  if (!confirm('Hapus event ini?')) return
  
  try {
    const response = await $fetch(`${config.public.apiBase}/api/events/${eventId}`, {
      method: 'DELETE',
      body: { phoneNumber }
    })
    
    if (response.success) {
      await loadDashboardData() // Refresh data
    } else {
      alert(response.message || 'Gagal menghapus event')
    }
  } catch (err) {
    console.error('Delete event error:', err)
    alert('Gagal menghapus event')
  }
}

// Setup motivation
const setupMotivation = async () => {
  settingMotivation.value = true
  
  try {
    const response = await $fetch(`${config.public.apiBase}/api/motivation`, {
      method: 'POST',
      body: {
        phoneNumber,
        time: motivationTime.value,
        active: true
      }
    })
    
    if (response.success) {
      showMotivationModal.value = false
      await loadDashboardData() // Refresh data
    } else {
      alert(response.message || 'Gagal mengatur motivasi')
    }
  } catch (err) {
    console.error('Setup motivation error:', err)
    alert('Gagal mengatur motivasi')
  } finally {
    settingMotivation.value = false
  }
}

// Toggle motivation
const toggleMotivation = async (active) => {
  try {
    const response = await $fetch(`${config.public.apiBase}/api/motivation`, {
      method: 'POST',
      body: {
        phoneNumber,
        active
      }
    })
    
    if (response.success) {
      await loadDashboardData() // Refresh data
    } else {
      alert(response.message || 'Gagal mengubah pengaturan motivasi')
    }
  } catch (err) {
    console.error('Toggle motivation error:', err)
    alert('Gagal mengubah pengaturan motivasi')
  }
}

// Refresh data
const refreshData = () => {
  loadDashboardData()
}

// Logout
const logout = () => {
  navigateTo('/')
}

// Load data on mount
onMounted(() => {
  if (!phoneNumber) {
    navigateTo('/')
    return
  }
  
  // Validate phone number format
  const cleanPhone = phoneNumber.replace(/\D/g, '')
  if (!cleanPhone.startsWith('62')) {
    navigateTo('/')
    return
  }
  
  // Check if mobile
  checkIfMobile()
  window.addEventListener('resize', checkIfMobile)
  
  loadDashboardData()
})

// Set default datetime for new event
watch(showCreateEventModal, (newVal) => {
  if (newVal) {
    const now = new Date()
    
    // If a date is selected, use that date with default time
    if (selectedDate.value) {
      const defaultDateTime = new Date(selectedDate.value)
      defaultDateTime.setHours(now.getHours() + 1, 0, 0, 0)
      newEvent.value.datetime = defaultDateTime.toISOString().slice(0, 16)
    } else {
      // Use current time + 1 hour
      now.setHours(now.getHours() + 1)
      newEvent.value.datetime = now.toISOString().slice(0, 16)
    }
  }
})

// Cleanup
onUnmounted(() => {
  window.removeEventListener('resize', checkIfMobile)
})
</script>