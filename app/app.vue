<template>
  <div class="min-h-screen bg-[#FDFBF7] font-sans text-slate-800 selection:bg-orange-200 selection:text-orange-900">

    <nav class="px-2 lg:px-16 fixed top-0 w-full z-50 transition-all duration-300"
      :class="scrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-4' : 'bg-transparent py-6'">
      <div class="container mx-auto px-6 flex justify-between items-center">
        <div class="flex items-center gap-3">
          <img src="/logo.png" alt="MUBK Logo" class="h-10 md:h-12 w-auto object-contain" />
        </div>

        <div class="hidden md:flex space-x-8 text-sm font-semibold"
          :class="scrolled ? 'text-slate-600' : 'text-slate-700'">
          <a href="#program" class="hover:text-orange-600 transition">Tentang Program</a>
          <a href="#biaya" class="hover:text-orange-600 transition">Investasi</a>
          <a href="#jadwal" class="hover:text-orange-600 transition">Jadwal</a>
        </div>

        <a :href="paymentLink"
          class="hidden md:inline-flex items-center justify-center px-6 py-2.5 text-sm font-bold text-white transition-all duration-200 bg-[#4A3B32] rounded-full hover:bg-orange-600 hover:shadow-lg hover:shadow-orange-500/30">
          Daftar Sekarang
        </a>
      </div>
    </nav>

    <div class="relative pt-32 pb-10 md:pt-40 md:pb-20 px-4 lg:px-16 container mx-auto">
      <div class="text-center max-w-4xl mx-auto mb-12">
        <div
          class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-orange-100/50 border border-orange-200 text-orange-700 text-xs font-bold uppercase tracking-wider mb-6">
          <span class="w-2 h-2 rounded-full bg-orange-500 animate-pulse"></span>
          Program Spesial Ramadhan 1447 H
        </div>
        <h1 class="text-4xl md:text-6xl lg:text-7xl font-extrabold text-[#4A3B32] tracking-tight leading-[1.1] mb-6">
          Siap Ramadhan dengan <br />
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-orange-500 to-amber-500">Bahasa
            Al-Qur'an.</span>
        </h1>
        <p class="text-lg md:text-xl text-slate-500 max-w-2xl mx-auto leading-relaxed">
          Kelas Persiapan Bahasa Arab Dasar (BADAR). Belajar dari nol dalam 15 pertemuan intensif di bulan suci
          Ramadhan.
        </p>
      </div>

      <div
        class="relative w-full aspect-[4/3] md:aspect-[3/1] rounded-[2rem] md:rounded-[3rem] overflow-hidden shadow-2xl shadow-[#4A3B32]/10 group">
        <img
          src="https://images.unsplash.com/photo-1535552081922-631f7dea1e9d?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjR8fGFyYWJpY3xlbnwwfHwwfHx8MA%3D%3D"
          alt="Belajar" class="w-full h-full object-cover transition duration-1000 group-hover:scale-105" />
        <div class="absolute inset-0 bg-gradient-to-t from-[#4A3B32]/80 via-transparent to-transparent"></div>

        <div class="absolute bottom-8 left-8 hidden md:block text-white">
          <p class="text-sm font-medium opacity-90 mb-1">Periode Belajar</p>
          <p class="text-2xl font-bold">16 Februari 2026</p>
        </div>
      </div>
    </div>

    <div id="program" class="container mx-auto px-4 lg:px-16 mb-24">
      <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4 md:gap-6">

        <div
          class="bg-white p-8 rounded-[2rem] border border-slate-100 shadow-sm md:col-span-2 hover:border-orange-200 transition duration-300 group">
          <div
            class="w-12 h-12 bg-orange-100 rounded-2xl flex items-center justify-center text-orange-600 mb-6 group-hover:scale-110 transition">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z">
              </path>
            </svg>
          </div>
          <h3 class="text-2xl font-bold text-[#4A3B32] mb-3">Kenapa Gabung Ramadhan Ini?</h3>
          <p class="text-slate-500 leading-relaxed mb-6">
            Jangan biarkan Ramadhan berlalu biasa saja. Isi hari-hari puasa dengan memahami bahasa Al-Qur'an. 
            Dapat ilmu, skill, dan insyaallah pahala berlipat dalam satu paket.
          </p>
          <ul class="space-y-3">
            <li class="flex items-center gap-3 text-sm font-medium text-slate-700">
              <div class="w-5 h-5 rounded-full bg-green-100 text-green-600 flex items-center justify-center">✓</div>
              Senin – Jum'at (Intensif)
            </li>
            <li class="flex items-center gap-3 text-sm font-medium text-slate-700">
              <div class="w-5 h-5 rounded-full bg-green-100 text-green-600 flex items-center justify-center">✓</div>
              15x Pertemuan Total
            </li>
          </ul>
        </div>

        <div id="biaya"
          class="bg-[#4A3B32] p-8 rounded-[2rem] text-white flex flex-col justify-between relative overflow-hidden md:col-span-1 lg:col-span-1 shadow-lg shadow-[#4A3B32]/20 group">
          <div
            class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] [background-size:16px_16px]">
          </div>

          <div class="relative z-10">
            <p class="text-orange-300 font-bold text-xs tracking-widest uppercase mb-2">Total Investasi</p>
            <div class="flex items-baseline gap-1">
              <span class="text-4xl font-extrabold">155rb</span>
            </div>
            <p class="text-sm text-gray-400 mt-1">sudah termasuk pendaftaran</p>
          </div>

          <div class="relative z-10 mt-8 space-y-3">
            <div class="p-3 bg-white/5 rounded-xl border border-white/10 backdrop-blur-sm">
              <p class="text-xs text-gray-300 mb-1">Fasilitas</p>
              <p class="text-sm font-medium">Rekaman & Sertifikat</p>
            </div>
            <a :href="paymentLink"
              class="block w-full text-center py-3 bg-orange-600 hover:bg-orange-500 rounded-xl font-bold text-sm transition">
              Daftar Sekarang
            </a>
          </div>
        </div>

        <div
          class="bg-orange-50 p-8 rounded-[2rem] border border-orange-100 flex flex-col justify-center items-center text-center relative overflow-hidden group">
          <div
            class="absolute top-0 right-0 w-24 h-24 bg-orange-200 rounded-bl-[4rem] opacity-50 transition group-hover:scale-150 rounded-br-none">
          </div>
          <h3 class="text-lg font-bold text-[#4A3B32] mb-1 relative z-10">Buku Panduan</h3>
          <p class="text-3xl font-extrabold text-orange-600 mb-4 relative z-10">12 Jam</p>
          <p class="text-xs text-slate-500 relative z-10 mb-4 px-4">Modul ringkas khusus pemula untuk bisa baca dasar.
          </p>
          <a href="https://koleksi.mahadumar.id" target="_blank"
            class="text-xs font-bold text-[#4A3B32] underline hover:text-orange-600 relative z-10">
            Beli terpisah di sini &rarr;
          </a>
        </div>

        <div id="jadwal" class="bg-white p-8 rounded-[2rem] border border-slate-100 md:col-span-3 lg:col-span-4">
          <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-8 gap-4">
            <div>
              <h3 class="text-2xl font-bold text-[#4A3B32]">Pilihan Waktu Belajar</h3>
              <p class="text-slate-500 mt-1">Semua waktu mengacu pada WIB (Waktu Indonesia Barat)</p>
            </div>
            <span class="px-4 py-2 bg-slate-100 rounded-full text-xs font-bold text-slate-600">
              Via ZOOM Meeting
            </span>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
            <div
              class="p-5 rounded-2xl bg-[#FDFBF7] border border-[#EAE0D5] hover:border-orange-300 hover:shadow-md transition cursor-default group">
              <div class="text-2xl mb-2 group-hover:scale-110 transition duration-300 origin-left">🌅</div>
              <p class="font-bold text-[#4A3B32]">Kelas Pagi</p>
              <p class="text-2xl font-bold text-orange-600 my-1">05:30</p>
              <p class="text-xs text-slate-500">s/d 06:45 WIB</p>
            </div>
            <div
              class="p-5 rounded-2xl bg-[#FDFBF7] border border-[#EAE0D5] hover:border-orange-300 hover:shadow-md transition cursor-default group">
              <div class="text-2xl mb-2 group-hover:scale-110 transition duration-300 origin-left">🌤️</div>
              <p class="font-bold text-[#4A3B32]">Kelas Sore</p>
              <p class="text-2xl font-bold text-orange-600 my-1">16:00</p>
              <p class="text-xs text-slate-500">s/d 17:15 WIB</p>
            </div>
            <div
              class="p-5 rounded-2xl bg-[#FDFBF7] border border-[#EAE0D5] hover:border-orange-300 hover:shadow-md transition cursor-default group">
              <div class="text-2xl mb-2 group-hover:scale-110 transition duration-300 origin-left">🌙</div>
              <p class="font-bold text-[#4A3B32]">Kelas Malam</p>
              <p class="text-2xl font-bold text-orange-600 my-1">20:30</p>
              <p class="text-xs text-slate-500">s/d 21:45 WIB</p>
            </div>
          </div>
        </div>

      </div>
    </div>

    <footer class="bg-[#1A1614] text-slate-400 py-12 px-4 rounded-t-[3rem]">
      <div class="container mx-auto text-center">
        <img src="/logo.png" alt="Logo Footer" class="h-10 mx-auto mb-6 opacity-50" />
        <h3 class="text-white font-bold text-lg mb-2">Ramadhan Berkah, Belajar Lebih Terarah</h3>
        <p class="text-sm mb-8">Ma’had Umar bin Khattab Yogyakarta (YPIA Academy)</p>

        <div class="flex flex-wrap justify-center gap-6 text-sm">
          <a href="https://wa.me/6285786599931" class="hover:text-orange-500 transition">WA Admin Putra</a>
          <a href="https://wa.me/6281388982734" class="hover:text-orange-500 transition">WA Admin Putri</a>
          <a href="https://ypiaacademy.com" class="hover:text-orange-500 transition">YPIA Academy</a>
        </div>

        <div class="border-t border-white/10 mt-8 pt-8 text-xs">
          &copy; {{ new Date().getFullYear() }} MUBK. All rights reserved.
        </div>
      </div>
    </footer>

    <div
      class="fixed bottom-0 left-0 w-full bg-white border-t border-gray-100 p-4 md:hidden z-50 flex items-center justify-between shadow-[0_-4px_6px_-1px_rgba(0,0,0,0.1)]">
      <div>
        <p class="text-xs text-slate-500">Daftar sebelum 2 Feb</p>
        <p class="text-lg font-bold text-[#4A3B32]">Rp 155.000</p>
      </div>
      <a :href="paymentLink"
        class="bg-orange-600 text-white font-bold py-3 px-6 rounded-xl text-sm hover:bg-orange-700 transition">
        Daftar Sekarang
      </a>
    </div>

  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const paymentLink = 'https://app.sandbox.midtrans.com/payment-links/cbdfbe5a-a3bb-4b53-a292-db194e790687';
const scrolled = ref(false);

const handleScroll = () => {
  scrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

// Inject Google Font
useHead({
  title: 'Kelas Persiapan Ramadhan - MUBK',
  meta: [
    { name: 'theme-color', content: '#4A3B32' }
  ],
  link: [
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap' }
  ],
  style: [
    { children: 'body { font-family: "Plus Jakarta Sans", sans-serif; }' }
  ],
  link: [
    { rel: 'icon', type: 'image/png', href: '/logo.png' }
  ]
})
</script>