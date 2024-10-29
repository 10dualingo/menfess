<script setup lang="ts">
import IconArrowLeft from "virtual:icons/mdi/arrow-left";
</script>

<template>
  <main class="w-[40rem] px-6 py-12 text-left flex flex-col gap-y-2">
    <router-link
      to="/"
      class="underline text-gray-400 hover:text-gray-300 gap-x-1 active:text-gray-500 focus:outline-gray-400 transition inline-flex"
      ><IconArrowLeft class="my-auto" /> Balik ke menfess...</router-link
    >
    <h1 class="text-2xl font-bold mt-4">Kebijakan Privasi</h1>
    <p class="text-gray-400">Efektif dari tanggal 29 Oktober 2024.</p>
    <p class="text-gray-400">
      Pada Kelas 10.2, privasi Anda adalah prioritas utama kami. Kami
      berkomitmen untuk menyediakan platform yang anonim bagi pengguna untuk
      mengirim dan menerima pesan. Kebijakan Privasi ini menjelaskan bagaimana
      kami menangani data Anda untuk memastikan privasi Anda terlindungi.
    </p>
    <h2 class="text-xl font-bold mt-4">I. Pegumpulan Informasi</h2>
    <p class="text-gray-400">
      Kami tidak mengumpulkan informasi yang dapat digunakan untuk
      mengidentifikasi pengguna. Kami berjanji untuk tidak mengumpulkan,
      menyimpan, atau memproses nama, alamat email, nomor telepon, data lokasi,
      atau informasi pribadi lainnya. Privasi Anda adalah komitmen kami.
    </p>
    <h2 class="text-xl font-bold mt-4">II. Pemrosesan Pesan</h2>
    <p class="text-gray-400">
      Satu-satunya data yang kami proses adalah konten pesan yang Anda pilih
      untuk masukkan secara sukarela. Saat Anda mengirim pesan, kami memproses
      dan menyimpan konten pesan tersebut hanya untuk memfasilitasi
      pengirimannya ke penerima yang dituju.
    </p>
    <h2 class="text-xl font-bold mt-4">III. Pelacakan dan Analitik</h2>
    <p class="text-gray-400">
      Kami tidak menggunakan bentuk pelacakan, cookies, atau layanan analitik
      apapun yang dapat mengumpulkan data perilaku pengguna atau informasi
      pribadi. Aktivitas Anda di platform kami sepenuhnya anonim, dan tidak ada
      kebiasaan atau pola penelusuran yang dipantau.
    </p>
    <h2 class="text-xl font-bold mt-4">IV. Layanan Pihak Ketiga</h2>
    <p class="text-gray-400">
      Kami tidak menggunakan layanan pihak ketiga yang dapat mengumpulkan atau
      memproses data tentang Anda. Kami mengoperasikan platform kami secara
      independen, memastikan bahwa data Anda aman dan terjaga privasinya.
    </p>
    <h2 class="text-xl font-bold mt-4">V. Perbaruan Kebijakan Privasi</h2>
    <p class="text-gray-400">
      Kami dapat memperbarui Kebijakan Privasi ini dari waktu ke waktu. Setiap
      perubahan akan tercermin di halaman ini dengan "Tanggal Efektif" yang
      diperbarui. Kami mendorong pengguna untuk meninjau kebijakan ini secara
      berkala untuk tetap mengetahui setiap pembaruan.
    </p>
    <h2 class="text-xl font-bold mt-4">VI. Penutup</h2>
    <p class="text-gray-400">
      Jika Anda memiliki pertanyaan atau kekhawatiran terkait Kebijakan Privasi
      ini atau praktik Menfess 10.2, silakan hubungi kami di
      <a
        href="mailto:jason@pnxl.dev"
        class="underline text-blue-500 hover:text-blue-400 active:text-blue-600 focus:outline-blue-500 transition"
        >jason@pnxl.dev</a
      >.
    </p>
    <p class="text-gray-400">
      Dengan menggunakan dan mengirim pesan lewat Menfess 10.2, Anda menyetujui
      ketentuan Kebijakan Privasi ini.
    </p>
  </main>
</template>
