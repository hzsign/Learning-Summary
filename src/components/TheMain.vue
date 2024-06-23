<template>
  <div class="bg-green-50">
    <header
      class="sticky inset-x-0 top-0 z-10 bg-green-50 border-b-[1px] border-green-200"
    >
      <nav
        class="flex items-center justify-between p-6 lg:px-8"
        aria-label="Global"
      >
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Hz Sign</span>
            <img class="h-8 w-auto" src="/src/assets/hzsign.svg" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button
            type="button"
            class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = true"
          >
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a
            v-for="item in navigation"
            :key="item.name"
            :href="item.href"
            class="text-sm font-semibold leading-6 text-gray-900"
            >{{ item.name }}
          </a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <a
            href="https://linktr.ee/hzsign"
            target="_blank"
            class="text-sm font-semibold leading-6 text-gray-900"
            >Linktree <span aria-hidden="true">&rarr;</span></a
          >
        </div>
      </nav>
      <Dialog
        as="div"
        class="lg:hidden"
        @close="mobileMenuOpen = false"
        :open="mobileMenuOpen"
      >
        <div class="fixed inset-0 z-50" />
        <DialogPanel
          class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
        >
          <div class="flex items-center justify-between">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">Hz Sign</span>
              <img class="h-8 w-auto" src="@/assets/hzsign.svg" alt="" />
            </a>
            <button
              type="button"
              class="-m-2.5 rounded-md p-2.5 text-gray-700"
              @click="mobileMenuOpen = false"
            >
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a
                  @click="mobileMenuOpen = false"
                  v-for="item in navigation"
                  :key="item.name"
                  :href="item.href"
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                  >{{ item.name }}</a
                >
              </div>
              <div class="py-6">
                <a
                  href="https://linktr.ee/hzsign"
                  target="_blank"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                  >Linktree</a
                >
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>
    <div class="profil relative isolate py-12 px-8 pt-16">
      <img
        class="h-72 mx-auto rounded-full bg-origin-content p-4 border-4 border-dashed border-green-200"
        src="/src/assets/image.png"
        alt=""
      />
      <div
        class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
        aria-hidden="true"
      >
        <div
          class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#0BE339] to-[#8CFFA4] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
          style="
            clip-path: polygon(
              74.1% 44.1%,
              100% 61.6%,
              97.5% 26.9%,
              85.5% 0.1%,
              80.7% 2%,
              72.5% 32.5%,
              60.2% 62.4%,
              52.4% 68.1%,
              47.5% 58.3%,
              45.2% 34.5%,
              27.5% 76.7%,
              0.1% 64.9%,
              17.9% 100%,
              27.6% 76.8%,
              76.1% 97.7%,
              74.1% 44.1%
            );
          "
        />
      </div>
      <div class="mx-auto max-w-4xl py-12 sm:py-12 lg:py-20">
        <div class="text-center">
          <h1
            class="text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl tracking-wide"
          >
            Halo 👋🏼, saya Irfan, desainer kreatif yang berbasis di Indonesia.
          </h1>
        </div>
        <div class="flex justify-center mt-10">
          <div
            class="flex items-center justify-center gap-2 rounded-full px-3 py-2 text-sm leading-6 text-gray-600 ring-1 ring-gray-900/10 hover:ring-gray-900/20"
          >
            <a
              href="https://www.instagram.com/unpamofficial/"
              target="_blank"
              class="font-semibold text-grey-500"
              >Mahasiswa di
              <span class="font-semibold text-green-500"
                >Universitas Pamulang.</span
              >
            </a>
            <p>✍🏼</p>
          </div>
        </div>
      </div>
      <div
        class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
        aria-hidden="true"
      >
        <div
          class="relative left-[calc(50%+3rem)] aspect-[1200/375] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#0BE339] to-[#8CFFA4] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]"
          style="
            clip-path: polygon(
              74.1% 44.1%,
              100% 61.6%,
              97.5% 26.9%,
              85.5% 0.1%,
              80.7% 2%,
              72.5% 32.5%,
              60.2% 62.4%,
              52.4% 68.1%,
              47.5% 58.3%,
              45.2% 34.5%,
              27.5% 76.7%,
              0.1% 64.9%,
              17.9% 100%,
              27.6% 76.8%,
              76.1% 97.7%,
              74.1% 44.1%
            );
          "
        />
      </div>
    </div>
    <div
      id="mata-kuliah"
      class="mata-kuliah text-center bg-white pt-32 sm:pt-24"
    >
      <div class="mx-auto max-w-8xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:text-center">
          <h2 class="text-base font-semibold leading-7 text-green-500">
            Mata Kuliah
          </h2>
          <p
            class="sm:mb-8 lg:mb-8 mb-8 mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl"
          >
            Catatan Rangkuman Mata Kuliah Komputer dan Masyarakat
          </p>
        </div>
      </div>

      <div
        id="accordion-color"
        data-accordion="collapse"
        data-active-classes="bg-blue-100 dark:bg-gray-800 text-blue-600 dark:text-white"
        class="xl:py-8 xl:px-8 xl:pb-24 pb-16 px-2 text-left"
      >
        <h2 id="accordion-color-heading-1">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 rounded-t-xl focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-1"
            aria-expanded="true"
            aria-controls="accordion-color-body-1"
          >
            <span>Pertemuan 1</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-1"
          class="hidden"
          aria-labelledby="accordion-color-heading-1"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
          >
            <section>
              <h2 class="text-xl font-semibold mb-2">Uraian Materi</h2>
              <ol class="mb-4">
                <li>
                  <h3 class="font-semibold mb-2">Definisi Komputer</h3>
                  <p>
                    Komputer adalah alat elektronik yang dapat menerima data
                    (input), memproses data (proses), dan menghasilkan informasi
                    (output).
                  </p>
                  <br />
                </li>
                <li>
                  <h3 class="font-semibold mb-2">Generasi Komputer</h3>
                  <p>
                    Generasi komputer dibedakan berdasarkan bentuk, kegunaan,
                    tampilan, dan prosedur yang dilakukan.
                  </p>
                  <ul class="list-disc list-inside ml-6">
                    <li>Generasi Pertama (1941 - 1952)</li>
                    <li>Generasi Kedua (1952-1956-1958)</li>
                    <li>Generasi Ketiga (1958 – 1970)</li>
                    <li>Generasi Keempat (1970 – 1980)</li>
                    <li>Generasi Kelima (1980 – sekarang)</li>
                    <li>Generasi Keenam (Masa Depan)</li>
                  </ul>
                </li>
                <br />
                <li>
                  <h3 class="font-semibold mb-2">Penggolongan Komputer</h3>
                  <p>
                    Komputer dapat digolongkan berdasarkan beberapa kriteria,
                    antara lain processor, bentuk dan ukuran fisik, jenis data
                    yang diolah, dan penggunaannya.
                  </p>
                </li>
              </ol>
            </section>

            <section>
              <h2 class="font-semibold mb-2">Penutup</h2>
              <p class="mb-4">
                Komputer telah mengalami perkembangan yang pesat dari generasi
                ke generasi. Jenis-jenis komputer yang ada saat ini memiliki
                kemampuan yang jauh lebih canggih dibandingkan dengan komputer
                di masa lampau. Komputer memiliki peran penting dalam berbagai
                aspek kehidupan manusia.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-2">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-2"
            aria-expanded="false"
            aria-controls="accordion-color-body-2"
          >
            <span>Pertemuan 2</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-2"
          class="hidden"
          aria-labelledby="accordion-color-heading-2"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
          >
            <section>
              <h2 class="text-xl font-semibold mb-2">Uraian Materi</h2>
              <ol class="mb-4">
                <li>
                  <h3 class="font-semibold mb-2">Sejarah Awal Komputer</h3>
                  <ul class="list-disc list-inside ml-6">
                    <li>Sempoa</li>
                    <li>Kalkulator Roda Numerik</li>
                    <li>Kalkulator Mekanik</li>
                  </ul>
                </li>
                <br />
                <li>
                  <h3 class="font-semibold mb-2">
                    Sejarah Perkembangan Komputer
                  </h3>
                  <ul class="list-disc list-inside ml-6">
                    <li>Blaise Pascal</li>
                    <li>Charles Babbage</li>
                    <li>Herman Hollerith</li>
                    <li>Howard H. Aiken</li>
                    <li>John William Mauchly</li>
                  </ul>
                </li>
                <br />
                <li>
                  <h3 class="font-semibold mb-2">
                    Kritik Terhadap Perkembangan Teknologi Maju
                  </h3>
                  <p>
                    Teknologi dapat menindas dan mengubah makna menjadi tujuan,
                    ketergantungan masyarakat terhadap komputer semakin tinggi,
                    dan perkembangan teknologi dapat mengubah cara berpikir
                    manusia.
                  </p>
                </li>
                <br />
                <li>
                  <h3 class="font-semibold mb-2">
                    Dampak Positif Teknologi Komputer
                  </h3>
                  <ul class="list-disc list-inside ml-6">
                    <li>Mempermudah pekerjaan manusia</li>
                    <li>Mempercepat komunikasi</li>
                    <li>Meningkatkan efisiensi</li>
                    <li>Memperluas akses informasi</li>
                  </ul>
                </li>
                <br />
                <li>
                  <h3 class="font-semibold mb-2">
                    Dampak Negatif Teknologi Komputer
                  </h3>
                  <ul class="list-disc list-inside ml-6">
                    <li>Dapat menyebabkan kecanduan</li>
                    <li>Mempersempit interaksi sosial</li>
                    <li>Meningkatkan risiko penipuan dan cybercrime</li>
                    <li>Memperlebar kesenjangan digital</li>
                  </ul>
                </li>
              </ol>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Teknologi komputer memiliki dampak positif dan negatif bagi
                kehidupan manusia. Penting untuk menggunakan teknologi dengan
                bijak dan bertanggung jawab.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-3">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-3"
            aria-expanded="false"
            aria-controls="accordion-color-body-3"
          >
            <span>Pertemuan 3</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-3"
          class="hidden"
          aria-labelledby="accordion-color-heading-3"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <p class="font-bold">Masyarakat:</p>
            <ul class="ps-5 list-disc">
              <li>
                Definisi masyarakat sebagai kumpulan individu yang saling
                berhubungan dan bergantung satu sama lain.
              </li>
              <li>
                Perspektif beberapa pakar seperti Max Weber, Selo Soemardjan,
                dan Emile Durkheim mengenai masyarakat.
              </li>
              <li>
                Pentingnya interaksi dan hubungan antarindividu dalam
                masyarakat.
              </li>
            </ul>
            <br />
            <p class="font-bold">Dinamika Masyarakat:</p>
            <ul class="ps-5 list-disc">
              <li>
                Perubahan yang terjadi dalam lingkungan yang dinamis,
                membutuhkan adaptasi manusia.
              </li>
              <li>
                Contoh perubahan sosial yang terjadi dalam kehidupan
                sehari-hari, misalnya: <br />
                1. Komputer memungkinkan pekerjaan dapat dilakukan dengan cepat
                dan akurat, mempercepat proses produksi, pengelolaan data, dan
                komunikasi. <br />
                2. Melalui internet, komputer memungkinkan akses cepat terhadap
                berbagai informasi, pengetahuan, dan sumber daya pendidikan.
                <br />
                3. Komputer digunakan dalam pembelajaran jarak jauh, e-learning,
                dan pengajaran interaktif, memungkinkan akses pendidikan yang
                lebih luas dan fleksibel.
              </li>
            </ul>
            <br />
            <p class="font-bold">Pemanfaatan Komputer:</p>
            <ul class="ps-5 list-disc">
              <li>
                Peran dan pengaruh komputer dalam kehidupan sehari-hari manusia.
              </li>
              <li>
                Komputer sebagai alat pengolah data dan contoh penggunaannya.
              </li>
              <li>
                Manfaat komputer dalam berbagai bidang seperti kesehatan,
                transportasi, pendidikan, jasa pengiriman barang, konstruksi,
                pertahanan negara, industri, jasa, perfilman, rekaman, dan
                olahraga.
              </li>
            </ul>
            <br />
            <p class="font-bold">Dampak Akibat Adanya Komputer:</p>
            <ul class="ps-5list-disc">
              <li>Dampak positif dan negatif dari keberadaan komputer.</li>
              <li>
                Isu-isu sosial yang muncul seiring dengan penggunaan teknologi
                komputer, seperti dampak pada pekerjaan, kesehatan, hak
                kebebasan pribadi, kendali yang terpusat, tanggung jawab, citra
                diri manusia, etika dan profesionalisme, kepentingan nasional,
                dan kesenjangan keahlian.
              </li>
            </ul>
            <br />
            <p>
              Materi pertemuan ke-3 ini membahas tentang pentingnya pemanfaatan
              komputer dalam masyarakat serta dampak yang ditimbulkannya. Dengan
              memahami berbagai aplikasi komputer dan isu-isu sosial yang
              terkait, diharapkan mahasiswa dapat menjadi lebih aware dan
              kompeten dalam menghadapi perkembangan teknologi di era digital
              ini.
            </p>
          </div>
        </div>
        <h2 id="accordion-color-heading-4">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-4"
            aria-expanded="false"
            aria-controls="accordion-color-body-4"
          >
            <span>Pertemuan 4</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-4"
          class="hidden"
          aria-labelledby="accordion-color-heading-4"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Uraian Materi:</h2>

              <h3 class="text-lg font-semibold mb-2">
                Perubahan Pola Pendidikan:
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>Pendidikan terbuka (Kampus Merdeka)</li>
                <li>Sharing resource (perpustakaan digital)</li>
                <li>
                  Penerapan teknologi multimedia terbaru (menggantikan teknologi
                  lama)
                </li>
                <li>Metode pembelajaran jarak jauh (E-learning)</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                Platform Pembelajaran Online:
              </h3>

              <h4 class="text-md font-semibold mb-1">Microsoft Office 365</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: fitur selalu up to date, penyimpanan OneDrive 1TB,
                  bonus Skype, diakses lebih dari 1 PC, dukungan penuh dari
                  Office
                </li>
                <li>
                  Kekurangan: harus berlangganan, harus terhubung internet
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Ruang Guru</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: penampilan menarik, materi lengkap, kualitas video
                  bagus, pembelajaran tidak membosankan, rangkuman materi mudah
                  dipahami, kuis dan latihan soal, interaksi antar siswa, tutor
                  online, kelas belajar streaming, konseling gratis
                </li>
                <li>
                  Kekurangan: volume bantuan suara terlalu tinggi, antarmuka
                  ramai, penyampaian video childish, iklan promosi
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Rumah Belajar</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: konten menarik, offline/online, tujuan pembelajaran
                  jelas, interaktif, gratis, nilai hasil kerja siswa, penjelasan
                  soal, percobaan matematika dan IPA, eksplorasi planet, diklat
                  online, kelas maya, penilaian tugas, kuis dan latihan,
                  aplikasi mudah dipahami
                </li>
                <li>
                  Kekurangan: materi belum lengkap, pilihan buku terbatas, sulit
                  menuliskan soal, bank soal belum terlink ke kelas maya,
                  percobaan laboratorium terbatas, budaya belum lengkap di peta
                  budaya, web berat di fitur antariksa, diklat terbatas, sulit
                  menulis jawaban di kelas maya dengan equation, kelas maya
                  belum terlink ke bank soal
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Meja Kita</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: bertukar catatan/rumus, diskusi antar siswa,
                  penghasilan tambahan bagi siswa yang menjawab pertanyaan atau
                  membagikan catatan
                </li>
                <li>
                  Kekurangan: mengarah ke bisnis/komersial, rentan menyontek
                  jawaban
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Edmodo</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: tampilan sederhana, bisa membagikan file, aplikasi
                  mobile
                </li>
                <li>
                  Kekurangan: tidak terintegrasi dengan sosial media, hanya
                  bahasa Inggris, tidak ada video conference
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Moodle</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: networking dan security yang dapat diatur sendiri,
                  ruang akses dibatasi, sistem pembelajaran dapat disesuaikan,
                  fitur lengkap, proses customize mudah, lesson yang fleksibel
                </li>
                <li>
                  Kekurangan: harus paham sistem Moodle, perlu tenaga ahli,
                  perangkat mahal
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">SEVIMA EdLink</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Kelebihan: reminder jadwal perkuliahan, diskusi kelas</li>
                <li>Kekurangan: sangat tergantung pada kecepatan internet</li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Google Classroom</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: mudah digunakan, file tersimpan di Google Drive
                </li>
                <li>
                  Kekurangan: tampilan kurang menarik, waktu pengiriman tugas
                  dapat diatur
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Kelas Kita</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Kelebihan: memilih kelas sesuai minat, fitur sosial media,
                  digunakan berbagai kalangan, gratis, kelas umum/khusus,
                  penghasilan tambahan dari kelas gratis, sertifikat digital
                </li>
                <li>Kekurangan: mengarah ke bisnis/komersial</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Dampak Metode Pembelajaran Online:
              </h2>

              <h3 class="text-lg font-semibold mb-2">Dampak Positif:</h3>
              <ul class="list-disc list-inside mb-4">
                <li>E-learning sebagai metode pembelajaran informal</li>
                <li>Mengakses ilmu dari banyak sumber</li>
                <li>Mendukung pembelajaran kelompok</li>
                <li>Efisien dalam penggunaan waktu</li>
                <li>Menghemat biaya pendidikan</li>
                <li>Kemudahan mengakses materi belajar</li>
                <li>Menjangkau wilayah geografis yang luas</li>
                <li>Siswa lebih mandiri</li>
                <li>Siswa diberi kebebasan untuk berkreasi</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">Dampak Negatif:</h3>
              <ul class="list-disc list-inside mb-4">
                <li>Kurangnya interaksi</li>
                <li>Mengabaikan aspek sosial</li>
                <li>Proses belajar kearah pelatihan</li>
                <li>Penambahan tugas untuk pendidik</li>
                <li>Cenderung gagal bagi siswa bermotivasi rendah</li>
                <li>Tergantung pada jaringan internet</li>
                <li>Keterampilan internet belum cukup</li>
                <li>Kurangnya keterampilan komunikasi siswa</li>
                <li>Berkurangnya praktik nyata</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan:</h2>
              <p class="mb-4">
                Teknologi informasi dan komunikasi membawa perubahan besar dalam
                dunia pendidikan. E-learning menjadi metode pembelajaran yang
                populer dengan berbagai platform dan aplikasi yang tersedia.
                E-learning memiliki dampak positif dan negatif bagi siswa dan
                pendidik. Pemanfaatan E-learning yang efektif membutuhkan
                persiapan yang matang dan kerjasama antara semua pihak involved.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-5">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-5"
            aria-expanded="false"
            aria-controls="accordion-color-body-5"
          >
            <span>Pertemuan 5</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-5"
          class="hidden"
          aria-labelledby="accordion-color-heading-5"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Uraian Materi:</h2>

              <h3 class="text-lg font-semibold mb-2">1. E-government:</h3>
              <p class="mb-2">
                <strong>Definisi:</strong> Penggunaan teknologi digital untuk
                meningkatkan efektivitas dan efisiensi layanan publik.
              </p>
              <h4 class="text-md font-semibold mb-1">Manfaat:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Meningkatkan kualitas layanan publik.</li>
                <li>Meningkatkan keterbukaan dan akuntabilitas pemerintah.</li>
                <li>Menghemat biaya administrasi.</li>
                <li>Meningkatkan partisipasi masyarakat.</li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Tujuan:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Meningkatkan mutu pelayanan kepada masyarakat.</li>
                <li>Memenuhi kebutuhan informasi masyarakat.</li>
                <li>Meningkatkan perekonomian.</li>
                <li>Meningkatkan transparansi dan akuntabilitas pemerintah.</li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Pemicu Utama:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Era globalisasi dan tuntutan masyarakat.</li>
                <li>Kemajuan teknologi informasi dan komunikasi.</li>
                <li>
                  Peningkatan kualitas pola pikir dan kegiatan masyarakat.
                </li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Strategi Pengembangan:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Membangun sistem pelayanan yang mudah diakses dan terpercaya.
                </li>
                <li>
                  Mengembangkan industri telekomunikasi dan teknologi informasi.
                </li>
                <li>Meningkatkan manajemen proses kerja pemerintah.</li>
                <li>
                  Memanfaatkan teknologi dalam industri telekomunikasi dan
                  informasi.
                </li>
                <li>Melakukan pengembangan secara sistematis dan terukur.</li>
                <li>Meningkatkan kapasitas SDM dan e-literacy masyarakat.</li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Contoh Aplikasi:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>mCity: Aplikasi informasi kota.</li>
                <li>Qlue: Aplikasi pelaporan kerusakan fasilitas publik.</li>
                <li>Lapor!: Aplikasi pengaduan masyarakat.</li>
                <li>Info BMKG: Aplikasi informasi cuaca dan gempa.</li>
                <li>
                  BPOM Mobile: Aplikasi informasi produk obat dan makanan.
                </li>
              </ul>
            </section>

            <section>
              <h3 class="text-lg font-semibold mb-2">
                2. Tugas Humas Pemerintah:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Memberikan informasi yang jelas dan benar kepada masyarakat.
                </li>
                <li>Memastikan kerjasama dan kepatuhan terhadap kebijakan.</li>
                <li>Mendukung kebijakan dan program pemerintah.</li>
                <li>Menyampaikan aspirasi masyarakat kepada pemerintah.</li>
              </ul>
            </section>

            <section>
              <h3 class="text-lg font-semibold mb-2">
                3. Isu Sosial dan Masalah:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Keamanan siber.</li>
                <li>Kurangnya interaksi sosial.</li>
                <li>Kurangnya pengetahuan masyarakat.</li>
                <li>Keterbatasan pelayanan.</li>
                <li>Keterbatasan anggaran.</li>
                <li>Keamanan informasi dan standarisasi.</li>
                <li>Kesenjangan akses internet.</li>
                <li>Ketidakmerataan penerapan e-government.</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan:</h2>
              <p class="mb-4">
                E-government merupakan alat penting untuk meningkatkan kualitas
                layanan publik dan pemerintahan. Namun, penerapannya perlu
                diiringi dengan strategi yang matang dan solusi untuk mengatasi
                berbagai isu sosial dan masalah yang muncul.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-6">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-6"
            aria-expanded="false"
            aria-controls="accordion-color-body-6"
          >
            <span>Pertemuan 6</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-6"
          class="hidden"
          aria-labelledby="accordion-color-heading-6"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Uraian Materi:</h2>

              <h3 class="text-lg font-semibold mb-2">1. Revolusi Industri:</h3>
              <p class="mb-2">
                Era revolusi industri mengubah cara hidup dan kerja manusia di
                berbagai bidang. Ditandai dengan perkembangan teknologi
                informasi dan kecerdasan buatan.
              </p>
              <p class="mb-2">Terbagi menjadi beberapa tahap:</p>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  <strong>Industri 1.0:</strong> Penggunaan mesin uap dan air
                  untuk membantu pekerja.
                </li>
                <li><strong>Industri 2.0:</strong> Penemuan energi listrik.</li>
                <li>
                  <strong>Industri 3.0:</strong> Penggunaan perangkat elektronik
                  dan sistem dengan perangkat lunak.
                </li>
                <li>
                  <strong>Industri 4.0:</strong> Penggunaan internet dan otomasi
                  dalam proses produksi.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">2. Otomasi Industri:</h3>
              <p class="mb-2">
                Proses produksi yang dilakukan oleh mesin dengan tujuan
                meningkatkan kualitas dan kuantitas.
              </p>
              <h4 class="text-md font-semibold mb-1">Manfaatnya:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Meningkatkan kualitas produk.</li>
                <li>Meningkatkan manajemen produksi.</li>
                <li>Meningkatkan jumlah produksi.</li>
                <li>Menghemat sumber daya.</li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Dampak negatifnya:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Mengurangi kesempatan kerja.</li>
                <li>
                  Membutuhkan biaya perawatan dan pemeliharaan yang tinggi.
                </li>
                <li>Membutuhkan sumber daya manusia yang terampil.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">3. Struktur Robotik:</h3>
              <p class="mb-2">
                Terdiri dari manipulator, kontroler, power supply, dan end
                effector. Digunakan untuk menggantikan pekerjaan manusia yang
                membutuhkan ketelitian dan kecepatan tinggi.
              </p>
              <h4 class="text-md font-semibold mb-1">Manfaatnya:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Meningkatkan kualitas produk.</li>
                <li>Meningkatkan efisiensi produksi.</li>
                <li>Mengurangi risiko kecelakaan kerja.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                4. Jenis Penggunaan Komputer dalam Bidang Industri:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  <strong>CAD (Computer Aided Design):</strong> Digunakan untuk
                  membantu desain gambar 3 dimensi.
                </li>
                <li>
                  <strong>CAM (Computer-Aided Manufacturing):</strong> Digunakan
                  untuk mengoperasikan mesin produksi.
                </li>
                <li>
                  <strong>MRPII (Manufacturing Resource Planning):</strong>
                  Digunakan untuk membuat rancangan sumber daya produksi skala
                  besar.
                </li>
                <li>
                  <strong>CIM (Computer Integrated Manufacturing):</strong>
                  Digunakan untuk mengontrol seluruh proses produksi.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                5. Kegunaan Komputer di Bidang Industri:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Membantu proses produksi massal.</li>
                <li>Membantu proses pengemasan.</li>
                <li>Membantu proses distribusi dan promosi.</li>
                <li>Membantu proses administrasi.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                6. Dampak Negatif Penggunaan Komputer dalam Bidang Industri:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Biaya perawatan dan pemeliharaan mesin dan robot yang tinggi.
                </li>
                <li>Mengurangi kesempatan kerja.</li>
                <li>Pemborosan energi.</li>
                <li>Kurangnya sumber daya manusia yang terampil.</li>
                <li>Bersifat konsumtif.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                7. Peluang dan Tantangan Industri 4.0:
              </h3>
              <h4 class="text-md font-semibold mb-1">Peluang:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Memperluas akses informasi dan komunikasi.</li>
                <li>Membuka peluang bisnis baru.</li>
                <li>Meningkatkan efisiensi dan produktivitas.</li>
              </ul>

              <h4 class="text-md font-semibold mb-1">Tantangan:</h4>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Pengangguran.</li>
                <li>Kesenjangan digital.</li>
                <li>Keamanan siber.</li>
                <li>Ancaman terhadap privasi.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                8. Isu Terkait dengan Revolusi Industri di Kalangan Masyarakat:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  <strong>Peran tenaga kerja:</strong> Apakah akan digantikan
                  oleh mesin?
                </li>
                <li>
                  <strong>Pemutusan Hak Kerja (PHK):</strong> Apakah akan
                  semakin banyak terjadi?
                </li>
                <li>
                  <strong>Kesiapan masyarakat:</strong> Bagaimana agar
                  masyarakat siap dengan perubahan?
                </li>
                <li>
                  <strong>Sosialisasi oleh pemerintah:</strong> Apakah
                  pemerintah akan melakukan sosialisasi kepada masyarakat?
                </li>
                <li>
                  <strong>Keterbatasan akses internet:</strong> Bagaimana
                  menanggulangi keterbatasan masyarakat terhadap penggunaan
                  internet?
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan:</h2>
              <p class="mb-4">
                Revolusi industri 4.0 membawa banyak peluang dan tantangan bagi
                industri dan masyarakat. Penting bagi pemerintah, industri, dan
                masyarakat untuk bekerja sama dalam mempersiapkan diri
                menghadapi perubahan ini.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-7">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-7"
            aria-expanded="false"
            aria-controls="accordion-color-body-7"
          >
            <span>Pertemuan 7</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-7"
          class="hidden"
          aria-labelledby="accordion-color-heading-7"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Topik:</h2>
              <ul class="list-disc list-inside mb-4">
                <li>Pengertian dan ciri-ciri masyarakat informasi</li>
                <li>
                  Faktor-faktor yang mendorong terbentuknya masyarakat informasi
                </li>
                <li>
                  Pengaruh masyarakat informasi terhadap berbagai aspek
                  kehidupan
                </li>
                <li>Peranan internet dalam masyarakat informasi</li>
                <li>Aplikasi internet yang umum digunakan</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Poin-poin penting:</h2>

              <h3 class="text-lg font-semibold mb-2">Masyarakat informasi:</h3>
              <p class="mb-2">
                Masyarakat yang memiliki minat tinggi terhadap informasi dan
                menggunakan teknologi informasi untuk mengaksesnya.
              </p>

              <h3 class="text-lg font-semibold mb-2">
                Ciri-ciri masyarakat informasi:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  Menjadikan internet sebagai infrastruktur kehidupan
                  sehari-hari.
                </li>
                <li>Informasi menjadi sumber utama dalam dunia usaha.</li>
                <li>Informasi menjadi aset bagi siapa saja.</li>
                <li>Terdapat sistem pelayanan online.</li>
                <li>Adanya persaingan yang ketat dan bersifat global.</li>
                <li>Proses pertukaran informasi yang sangat cepat.</li>
                <li>
                  Menjadikan informasi sebagai pendongkrak berkembangnya usaha.
                </li>
                <li>
                  Menggunakan informasi sebagai pertimbangan untuk mengambil
                  suatu keputusan.
                </li>
                <li>
                  Terjadinya komunikasi hampir secara instan melintasi jarak
                  yang begitu jauh.
                </li>
                <li>Cepatnya proses penyerapan informasi.</li>
                <li>
                  Menjadikan informasi sebagai salah satu komoditi ekonomi yang
                  memiliki harga sesuai dengan.
                </li>
                <li>Tingginya nilai ketergantungan terhadap informasi.</li>
                <li>Tingginya tingkat responsibilitas terhadap informasi.</li>
                <li>
                  Pola hidup atau kehidupan sosial bisa dipengaruhi oleh
                  informasi.
                </li>
                <li>Masyarakat cenderung bersifat lebih demokratis.</li>
                <li>
                  Cara mengakses informasi berubah dari media cetak ke media
                  online.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                Faktor-faktor yang mendorong terbentuknya masyarakat informasi:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Tuntutan dari efek perkembangan zaman.</li>
                <li>Dinamika dalam komunikasi dan informasi.</li>
                <li>Berkembangnya teknologi komputer.</li>
                <li>Berkembangnya teknologi informasi.</li>
                <li>Perubahan karakteristik pola kerja.</li>
                <li>Adanya perubahan cara penyebaran informasi.</li>
                <li>Adanya perubahan cara penyebaran pengetahuan.</li>
                <li>
                  Tingginya minat masyarakat terhadap teknologi informasi.
                </li>
                <li>
                  Sifat ingin tahu yang tinggi dari masyarakat terhadap
                  informasi terbaru.
                </li>
                <li>Melakukan suatu pekerjaan dengan mudah.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                Pengaruh masyarakat informasi terhadap berbagai aspek kehidupan:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>
                  <strong>Ekonomi:</strong> Munculnya peluang usaha baru,
                  persaingan yang lebih ketat, dan perubahan pola kerja.
                </li>
                <li>
                  <strong>Sosial:</strong> Meningkatnya keterbukaan dan
                  partisipasi masyarakat, perubahan cara berkomunikasi dan
                  bersosialisasi, dan munculnya isu-isu sosial baru.
                </li>
                <li>
                  <strong>Budaya:</strong> Perubahan nilai-nilai budaya dan cara
                  pandang masyarakat, munculnya budaya digital, dan pelestarian
                  budaya melalui teknologi informasi.
                </li>
                <li>
                  <strong>Politik:</strong> Meningkatnya partisipasi politik
                  masyarakat, perubahan cara kampanye dan pemilihan umum, dan
                  munculnya demokrasi digital.
                </li>
                <li>
                  <strong>Pendidikan:</strong> Meningkatnya akses terhadap
                  informasi dan pendidikan, perubahan metode belajar mengajar,
                  dan munculnya e-learning.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                Peranan internet dalam masyarakat informasi:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Sebagai sumber informasi dan pengetahuan.</li>
                <li>Sebagai sarana komunikasi dan interaksi sosial.</li>
                <li>Sebagai alat untuk berbisnis dan berdagang.</li>
                <li>Sebagai media untuk hiburan dan rekreasi.</li>
                <li>Sebagai alat untuk belajar dan mengajar.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                Aplikasi internet yang umum digunakan:
              </h3>
              <ul class="list-disc list-inside ml-4 mb-4">
                <li>Media sosial (Facebook, Instagram, Twitter, dll.)</li>
                <li>Layanan pesan instan (WhatsApp, Telegram, Line, dll.)</li>
                <li>Mesin pencari (Google, Yahoo, Bing, dll.)</li>
                <li>Surel (Gmail, Yahoo Mail, Outlook, dll.)</li>
                <li>
                  Perbankan online (BRImo, Livin' by Mandiri, BNI Mobile
                  Banking, dll.)
                </li>
                <li>
                  Belanja online (Tokopedia, Shopee, Lazada, Blibli, dll.)
                </li>
                <li>
                  Layanan streaming video (YouTube, Netflix, Disney+, Vidio,
                  dll.)
                </li>
                <li>
                  Layanan streaming musik (Spotify, Apple Music, JOOX, Deezer,
                  dll.)
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan:</h2>
              <p class="mb-4">
                Masyarakat informasi telah membawa banyak perubahan dalam
                berbagai aspek kehidupan. Penting bagi kita untuk memahami
                perubahan-perubahan ini dan memanfaatkan teknologi informasi
                dengan bijak agar dapat memberikan manfaat bagi diri sendiri,
                masyarakat, dan bangsa.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-8">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-8"
            aria-expanded="false"
            aria-controls="accordion-color-body-8"
          >
            <span>Pertemuan 8</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-8"
          class="hidden"
          aria-labelledby="accordion-color-heading-8"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">
                A. Pengertian Masyarakat Informasi
              </h2>
              <p class="mb-2">
                Masyarakat informasi adalah masyarakat yang memiliki ciri-ciri:
              </p>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Menjadikan internet sebagai infrastruktur kehidupan
                  sehari-hari
                </li>
                <li>Informasi menjadi sumber utama dalam dunia usaha</li>
                <li>Informasi menjadi aset bagi siapa saja</li>
                <li>Terdapat sistem pelayanan online</li>
                <li>Adanya persaingan yang ketat dan bersifat global</li>
                <li>Proses pertukaran informasi yang sangat cepat</li>
                <li>
                  Menjadikan informasi sebagai pendongkrak berkembangnya usaha
                </li>
                <li>
                  Menggunakan informasi sebagai pertimbangan untuk mengambil
                  suatu keputusan
                </li>
                <li>
                  Terjadinya komunikasi hampir secara instan melintasi jarak
                  yang begitu jauh
                </li>
                <li>Cepatnya proses penyerapan informasi</li>
                <li>
                  Menjadikan informasi sebagai salah satu komoditi ekonomi yang
                  memiliki harga
                </li>
                <li>Tingginya nilai ketergantungan terhadap informasi</li>
                <li>Tingginya tingkat responsibilitas terhadap informasi</li>
                <li>
                  Pola hidup atau kehidupan sosial bisa dipengaruhi oleh
                  informasi
                </li>
                <li>Masyarakat cenderung bersifat lebih demokratis</li>
                <li>
                  Cara mengakses informasi berubah dari media cetak ke media
                  online
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                B. Dampak Teknologi Informasi Terhadap Masyarakat
              </h2>

              <h3 class="text-lg font-semibold mb-2">Dampak positif:</h3>
              <ul class="list-disc list-inside mb-4">
                <li>Arus informasi sangat cepat</li>
                <li>
                  Masyarakat dengan mudah mengakses informasi kapanpun mereka
                  mau
                </li>
                <li>
                  Wawasan masyarakat terhadap perkembangan dunia semakin luas
                </li>
                <li>Mempermudah pelaku bisnis untuk berbisnis secara online</li>
                <li>
                  Mempermudah masyarakat untuk berkomunikasi tanpa harus bertemu
                </li>
                <li>
                  Dapat digunakan sebagai sarana mencari informasi untuk bidang
                  pendidikan dan kebudayaan
                </li>
                <li>Sebagai sarana hiburan</li>
                <li>
                  Dengan berkembangnya teknologi informasi dan teknologi
                  komunikasi masyarakat lebih mudah beraktifitas
                </li>
                <li>
                  Wawasan masyarakat mengenai perkembangan teknologi makin luas
                </li>
                <li>
                  Terbukanya peluang usaha yang memanfaatkan jaringan internet
                </li>
                <li>Memberikan ruang untuk berkreasi bagi masyarakat</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">Dampak negatif:</h3>
              <ul class="list-disc list-inside mb-4">
                <li>Berkurangnya proses sosialisasi secara nyata</li>
                <li>Kejahatan dunia maya meningkat</li>
                <li>Konten negatif yang berkembang dengan pesat</li>
                <li>
                  Meningkatnya oknum yang memfitnah dan juga pencemaran nama
                  baik
                </li>
                <li>
                  Kecanduan terhadap internet bisa menyebabkan masyarakat tidak
                  produktif
                </li>
                <li>Berkurangnya pola interaksi dengan orang sekitar</li>
                <li>Terjadinya pelanggaran privasi</li>
                <li>Sifat plagiat makin bertambah</li>
                <li>Pembajakan hak cipta suatu karya</li>
                <li>Perjudian online meningkat</li>
                <li>Meningkatnya aksi pornografi</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                C. Penggunaan Teknologi Informasi di Masyarakat
              </h2>
              <p class="mb-2">
                Teknologi informasi digunakan di berbagai bidang, seperti:
              </p>
              <ul class="list-disc list-inside mb-4">
                <li>Perbankan</li>
                <li>Perdagangan</li>
                <li>Perindustrian</li>
                <li>Transportasi</li>
                <li>Kesehatan</li>
                <li>Pendidikan</li>
                <li>Seni</li>
                <li>Komunikasi</li>
                <li>Pertahanan dan Keamanan</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Masyarakat informasi telah membawa banyak perubahan dalam
                berbagai aspek kehidupan. Penting bagi kita untuk memahami
                perubahan-perubahan ini dan memanfaatkan teknologi informasi
                dengan bijak agar dapat memberikan manfaat bagi diri sendiri,
                masyarakat, dan bangsa.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-9">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-9"
            aria-expanded="false"
            aria-controls="accordion-color-body-9"
          >
            <span>Pertemuan 9</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-9"
          class="hidden"
          aria-labelledby="accordion-color-heading-9"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Uraian Materi</h2>

              <h3 class="text-lg font-semibold mb-2">
                1. Manfaat Komputer Dalam Bisnis
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Komputer membantu dalam administrasi keuangan, statistik
                  kemajuan, data stok barang, prediksi untuk penjualan, dan
                  bahkan untuk merencanakan bisnis masa depan.
                </li>
                <li>Contoh: mesin kasir, analisis data, e-commerce.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                2. Evolusi Pengolahan Data
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Tahap 1: menggantikan peran manusia dengan komputer untuk
                  menghemat biaya.
                </li>
                <li>
                  Tahap 2: mengalihkan SDM ke layanan, quality control,
                  operasional, analisa pengembangan sistem, dll.
                </li>
                <li>Tahap 3: pengendalian dalam pembelian dan penjualan.</li>
                <li>
                  Tahap 4: menganalisa data-data yang sudah di input, untuk
                  memprediksi penjualan kedepannya.
                </li>
              </ul>
              <p class="mb-4">
                Dampak: Profesi yang tergantikan (agen penjualan, kasir, teller,
                operator telepon, tukang pos, administrasi) dan munculnya
                profesi baru (programmer, data analyst, database administrator).
              </p>

              <h3 class="text-lg font-semibold mb-2">
                3. Dasar-dasar Database
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Database: sistem untuk menyimpan data dalam kapasitas besar
                  dengan efisien dan tidak akan terjadi redudansi data.
                </li>
                <li>Bagian utama database: data dan spreadsheet.</li>
                <li>
                  Proses pengolahan data: origination, input, processing,
                  output, distribution, storage.
                </li>
                <li>
                  Metode pemrosesan data: manual, electromechannical, punched
                  card equipment, electronic computer, network office.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                4. Sistem Manajemen Basisdata (DBMS)
              </h3>
              <p class="mb-2">
                Software khusus untuk mengolah data yang diinginkan di dalam
                basis data atau database.
              </p>
              <p class="mb-2">Tujuan DBMS:</p>
              <ul class="list-disc list-inside mb-4">
                <li>Memelihara data</li>
                <li>Mengganti tempat penyimpanan fisik</li>
                <li>Memperoleh data yang sama</li>
                <li>Agar basis data dapat digunakan secara bersamaan</li>
                <li>Proses pengolahan data cepat</li>
                <li>Tidak perlu menggunakan space yang besar</li>
                <li>Keamanan data terjaga</li>
                <li>Meminimalisir perubahan data</li>
                <li>Menghindari duplikasi data</li>
                <li>Bertanggung jawab untuk mengolah data yang besar</li>
                <li>Mendukung bahasa query</li>
                <li>Pengawasan backup database dan pemulihan dari kesalahan</li>
              </ul>
              <p class="mb-2">
                Software DBMS: MySQL, Oracle, Microsoft SQL Server, Firebird.
              </p>
              <p class="mb-2">Komponen DBMS:</p>
              <ul class="list-disc list-inside mb-4">
                <li>File Manager</li>
                <li>Database Manager</li>
                <li>Query Processor</li>
                <li>DML Precompiler</li>
                <li>DDL Compiler</li>
              </ul>
              <p class="mb-2">Kekurangan DBMS:</p>
              <ul class="list-disc list-inside mb-4">
                <li>Ukuran besar</li>
                <li>Kompleks</li>
                <li>Biaya</li>
                <li>Hardware</li>
                <li>Konversi</li>
                <li>Performa menurun</li>
                <li>kemungkinan kegagalan</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                5. Data Menguntungkan Bisnis
              </h3>
              <p class="mb-2">
                Mengumpulkan dan menganalisis data penting untuk meningkatkan
                efisiensi dan profit.
              </p>
              <p class="mb-2">Manfaat data:</p>
              <ul class="list-disc list-inside mb-4">
                <li>Memberikan pemahaman solid tentang pelanggan.</li>
                <li>
                  Mendapatkan pemahaman yang lebih dalam tentang penjualan.
                </li>
                <li>Kontrol stok yang efisien.</li>
                <li>Menanggapi perubahan.</li>
                <li>Analisis data.</li>
                <li>Meningkatkan keamanan data.</li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                6. Suatu Usaha Tidak Menggunakan Database
              </h3>
              <p class="mb-2">Alasan:</p>
              <ul class="list-disc list-inside mb-4">
                <li>Terlalu mahal.</li>
                <li>Terlalu mengganggu.</li>
                <li>Akan terlalu banyak waktu.</li>
                <li>Terlalu sulit untuk belajar dan melaksanakan.</li>
                <li>Terlalu rendah pada daftar prioritas.</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Penggunaan komputer dan database dalam dunia usaha sangatlah
                penting untuk meningkatkan efisiensi dan profit. Database
                membantu dalam berbagai aspek seperti administrasi keuangan,
                analisis data, prediksi penjualan, dan lain sebagainya. Meskipun
                ada beberapa kendala dalam penggunaan database, manfaatnya jauh
                lebih besar sehingga penting bagi pengusaha untuk
                mempelajarinya.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-10">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-10"
            aria-expanded="false"
            aria-controls="accordion-color-body-10"
          >
            <span>Pertemuan 10</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-10"
          class="hidden"
          aria-labelledby="accordion-color-heading-10"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Materi</h2>

              <h3 class="text-lg font-semibold mb-2">1. Definisi E-Commerce</h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Perdagangan elektronik meliputi aktivitas jual beli barang
                  atau penyebaran dan pemasaran barang dan jasa lewat media
                  elektronik.
                </li>
                <li>
                  Proses dalam E-Commerce: penjualan menggunakan website,
                  pemesanan otomatis, akun pelanggan aman, penjual
                  berpartisipasi di pasar online, penjualan B2B, pengumpulan
                  data untuk kontak, pertukaran data elektronik B2B, penggunaan
                  email dan newsletter, keterlibatan produsen dalam pra-retail,
                  pembayaran online, pelacakan pembelian.
                </li>
                <li>
                  E-Commerce muncul karena adanya internet dan teknologi
                  informasi.
                </li>
                <li>
                  E-Commerce mengacu pada pertukaran barang dan jasa yang
                  dilakukan oleh orang atau organisasi dengan dukungan sistem
                  teknologi informasi dan komunikasi.
                </li>
                <li>
                  Menurut Zwass (2014), E-Commerce berasal dari 5-C-model:
                  Commerce, Collaboration, Communication, Connection, dan
                  Computation.
                </li>
                <li>
                  E-Commerce menurunkan hambatan untuk masuk dalam penjualan
                  berbagai jenis barang.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                2. Model Bisnis E-Commerce
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Access Provider: memastikan pengguna E-Commerce dapat akses
                  internet.
                </li>
                <li>
                  Search Engine: perangkat lunak untuk mencari informasi di
                  internet.
                </li>
                <li>Online Shop: situs jual beli online.</li>
                <li>Content Provider: penyedia konten digital.</li>
                <li>
                  Online Marketplace/Electronic Mall: pasar online di mana
                  pemasok dan pelanggan dapat bertemu.
                </li>
                <li>
                  Virtual Community: platform untuk komunikasi dan pertukaran
                  pengalaman.
                </li>
                <li>
                  Information Broker: mengumpulkan dan memberikan informasi.
                </li>
                <li>Transaction Broker: mengeksekusi transaksi penjualan.</li>
                <li>
                  Online Service Provider/Cloud Service Provider (CSP):
                  menyediakan layanan yang dapat dijalankan secara elektronik.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                3. Kerugian dan Keuntungan E-Commerce
              </h3>
              <h4 class="text-md font-semibold mb-1">Keuntungan:</h4>
              <ul class="list-disc list-inside mb-4">
                <li>
                  <strong>Bagi Konsumen/Pelanggan:</strong> jam belanja
                  fleksibel, tidak antri, belanja dari mana saja, lebih banyak
                  kompetisi, layanan pelanggan lebih baik.
                </li>
                <li>
                  <strong>Bagi Penyedia Barang/Jasa:</strong> layanan pelanggan
                  lebih baik, komunikasi cepat dengan pelanggan, jangkauan
                  pelanggan luas, tidak ada perantara.
                </li>
              </ul>
              <h4 class="text-md font-semibold mb-1">Kerugian:</h4>
              <ul class="list-disc list-inside mb-4">
                <li>
                  <strong>Bagi Konsumen/Pelanggan:</strong> risiko keamanan
                  elektronik, pencurian data, pencurian identitas,
                  penyalahgunaan, kejahatan, penyedia barang/jasa fiktif,
                  penipuan, status hukum tidak pasti.
                </li>
                <li>
                  <strong>Bagi Penyedia Barang/Jasa:</strong> biaya logistik
                  lebih tinggi, pelanggan tidak jelas/penipu, kerusakan saat
                  pengiriman, penipuan.
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                4. Jenis Bisnis E-Commerce
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Consumer to Consumer (C2C): transaksi barang atau jasa yang
                  dilakukan konsumen ke konsumen.
                </li>
                <li>
                  Consumer to Business (C2B): transaksi jual beli produk atau
                  jasa dilakukan dari konsumen/perorangan kepada perusahaan.
                </li>
                <li>
                  Consumer/Citizen to Administrator/Government (C2A): proses
                  transaksi elektronik yang dilakukan individu kepada Lembaga
                  pemerintah.
                </li>
                <li>
                  Business to Consumer (B2C): proses transaksi yang dilakukan
                  antara produsen barang atau jasa langsung kepada konsumen
                  akhir.
                </li>
                <li>
                  Business to Business (B2B): proses transaksi online yang
                  dilakukan antar perusahaan atau jenis usaha barang atau jasa
                  secara tender atau lelang.
                </li>
                <li>
                  Business to Administration/Government (B2A): E-Commerce yang
                  menjual produk atau jasa kepada lembaga pemerintahan melalui
                  sistem tender.
                </li>
                <li>
                  Administration/Government to Consumer (A2C): pemerintah
                  membangun dan menerapkan portofolio teknologi informasi dengan
                  tujuan memperbaiki hubungan interaksi dengan masyarakat.
                </li>
                <li>
                  Administration/Government to Business (A2B): membentuk
                  lingkungan bisnis yang kondusif secara online agar
                  perekonomian sebuah negara berjalan dengan semestinya.
                </li>
                <li>
                  Administration/Government to Administration/Government (A2A):
                  kebutuhan interaksi antara satu pemerintah dengan pemerintah
                  lainnya setiap harinya dilakukan secara online.
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                E-Commerce merupakan cara perdagangan elektronik yang memiliki
                berbagai keuntungan dan kerugian. E-Commerce dapat dilakukan
                dengan berbagai model bisnis dan jenis transaksi. E-Commerce
                memberikan kemudahan dan efisiensi dalam berbisnis, namun juga
                memiliki risiko yang perlu diwaspadai.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-11">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-11"
            aria-expanded="false"
            aria-controls="accordion-color-body-11"
          >
            <span>Pertemuan 11</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-11"
          class="hidden"
          aria-labelledby="accordion-color-heading-11"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Materi</h2>

              <h3 class="text-lg font-semibold mb-2">
                1. Keamanan Sistem Informasi
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Keamanan sistem informasi adalah langkah-langkah untuk
                  melindungi sistem informasi dari akses tidak sah, pencurian
                  data, atau kerusakan.
                </li>
                <li>
                  Penting untuk menjaga keamanan sistem informasi karena:
                  <ul class="list-disc list-inside ml-6">
                    <li>Melindungi data penting.</li>
                    <li>Menjaga privasi.</li>
                    <li>Menjaga integritas data.</li>
                    <li>Mencegah gangguan operasional.</li>
                  </ul>
                </li>
                <li>
                  Jenis-jenis ancaman terhadap sistem informasi:
                  <ul class="list-disc list-inside ml-6">
                    <li>Malware (virus, worm, Trojan horse, dll.).</li>
                    <li>Hacker.</li>
                    <li>Social engineering.</li>
                    <li>Phishing.</li>
                    <li>Denial-of-service attack.</li>
                  </ul>
                </li>
                <li>
                  Langkah-langkah untuk mengamankan sistem informasi:
                  <ul class="list-disc list-inside ml-6">
                    <li>Gunakan password yang kuat dan ubah secara berkala.</li>
                    <li>Instal antivirus dan software keamanan lainnya.</li>
                    <li>Lakukan backup data secara rutin.</li>
                    <li>Perbarui perangkat lunak secara berkala.</li>
                    <li>Berhati-hatilah saat mengakses internet.</li>
                    <li>Edukasi pengguna tentang keamanan sistem informasi.</li>
                  </ul>
                </li>
              </ul>

              <h3 class="text-lg font-semibold mb-2">
                2. Etika dalam Penggunaan Komputer dan Informasi
              </h3>
              <ul class="list-disc list-inside mb-4">
                <li>
                  Etika adalah norma atau aturan yang mengatur perilaku manusia
                  dalam hubungannya dengan orang lain dan dengan masyarakat.
                </li>
                <li>
                  Etika dalam penggunaan komputer dan informasi meliputi:
                  <ul class="list-disc list-inside ml-6">
                    <li>Menghormati privasi orang lain.</li>
                    <li>
                      Tidak menggunakan komputer untuk merugikan orang lain.
                    </li>
                    <li>
                      Tidak menyalin atau menggunakan perangkat lunak ilegal.
                    </li>
                    <li>
                      Tidak menyebarkan informasi yang salah atau menyesatkan.
                    </li>
                    <li>
                      Bertanggung jawab atas tindakan yang dilakukan di
                      komputer.
                    </li>
                  </ul>
                </li>
                <li>
                  Sepuluh Perintah Etika Komputer:
                  <ul class="list-disc list-inside ml-6">
                    <li>
                      Tidak menggunakan komputer untuk merugikan orang lain.
                    </li>
                    <li>Tidak mengganggu pekerjaan komputer orang lain.</li>
                    <li>Tidak memata-matai file komputer orang lain.</li>
                    <li>Tidak menggunakan komputer untuk mencuri.</li>
                    <li>Tidak menggunakan komputer untuk bersaksi palsu.</li>
                    <li>
                      Tidak menyalin atau menggunakan kepemilikan perangkat
                      lunak dimana anda belum membayarnya.
                    </li>
                    <li>
                      Tidak menggunakan sumber daya komputer orang lain tanpa
                      otorisasi atau kompensasi yang sesuai.
                    </li>
                    <li>
                      Tidak mengambil untuk diri sendiri karya intelektual orang
                      lain.
                    </li>
                    <li>
                      Harus memikirkan tentang konsekuensi sosial program yang
                      anda tulis bagi sistem yang anda desain.
                    </li>
                    <li>
                      Harus menggunakan komputer yang menjamin pertimbangan dan
                      bagi sesama manusia.
                    </li>
                  </ul>
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Keamanan sistem informasi dan etika dalam penggunaan komputer
                dan informasi merupakan hal yang penting untuk dipahami dan
                diterapkan oleh semua pengguna komputer. Dengan menjaga keamanan
                sistem informasi dan menggunakan komputer secara etis, kita
                dapat melindungi data, menjaga privasi, dan membangun lingkungan
                digital yang aman dan kondusif.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-12">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-12"
            aria-expanded="false"
            aria-controls="accordion-color-body-12"
          >
            <span>Pertemuan 12</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-12"
          class="hidden"
          aria-labelledby="accordion-color-heading-12"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Topik</h2>
              <ul class="list-disc list-inside mb-4">
                <li>Kejahatan komputer</li>
                <li>Privasi</li>
                <li>Pengadilan kejahatan di dunia maya</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kejahatan Komputer</h2>
              <ul class="list-disc list-inside mb-4">
                <li>
                  <strong>Definisi:</strong> Tindakan ilegal yang menggunakan
                  pengetahuan komputer untuk tujuan kejahatan.
                </li>
                <li>
                  <strong>Contoh:</strong> Pencurian data, manipulasi data,
                  akses ilegal, penyebaran virus, dll.
                </li>
                <li>
                  <strong>Faktor peningkatan:</strong> Penggunaan internet,
                  transisi multi-vendor, kemudahan software, kemampuan pengguna,
                  penegakan hukum lemah.
                </li>
                <li>
                  <strong>Pencegahan:</strong> Gunakan password, ubah password,
                  gunakan antivirus, hati-hati di internet, backup data.
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Privasi</h2>
              <ul class="list-disc list-inside mb-4">
                <li>
                  <strong
                    >Hak untuk bebas dari intrusi ke dalam urusan
                    pribadi.</strong
                  >
                </li>
                <li>
                  <strong>Jenis:</strong> Privasi fisik (ruang, waktu, properti)
                  dan privasi informasi (data pribadi).
                </li>
                <li>
                  <strong>Pelanggaran:</strong> Membajak akun, menyebarkan data
                  pribadi, menjual data pelanggan, pemalsuan identitas.
                </li>
                <li>
                  <strong>UU ITE:</strong> Melarang penyebaran data pribadi
                  tanpa izin.
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Pengadilan Kejahatan Dunia Maya
              </h2>
              <ul class="list-disc list-inside mb-4">
                <li>
                  <strong>UU ITE:</strong> No. 19 Tahun 2016 tentang Perubahan
                  atas UU No. 11 Tahun 2008 tentang ITE.
                </li>
                <li>
                  <strong>Pasal karet:</strong> Istilah teknis yang berbeda di
                  dunia nyata dan teknologi.
                </li>
                <li>
                  <strong>Arti sempit:</strong> Kejahatan terhadap sistem
                  komputer dan data.
                </li>
                <li>
                  <strong>Arti luas:</strong> Kejahatan konvensional yang
                  menggunakan elektronik.
                </li>
                <li>
                  <strong>UU ITE:</strong>
                  <ul class="list-disc list-inside ml-6">
                    <li>
                      Penyebaran konten ilegal (kesusilaan, perjudian, dll.).
                    </li>
                    <li>Gangguan informasi/sistem elektronik.</li>
                    <li>Memfasilitasi perbuatan terlarang.</li>
                    <li>Pemalsuan informasi/dokumen elektronik.</li>
                  </ul>
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Keamanan komputer dan privasi penting di era digital. UU ITE
                mengatur kejahatan komputer dan pelanggaran privasi. Pengadilan
                dunia maya perlu mempertimbangkan konteks teknologi dan dunia
                nyata.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-13">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-13"
            aria-expanded="false"
            aria-controls="accordion-color-body-13"
          >
            <span>Pertemuan 13</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-13"
          class="hidden"
          aria-labelledby="accordion-color-heading-13"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">Topik</h2>
              <ul class="list-disc list-inside mb-4">
                <li>Pengertian etika dan etika profesi</li>
                <li>Ciri-ciri profesi dan profesionalisme</li>
                <li>Etika profesi di bidang IT</li>
                <li>Etika penggunaan teknologi informasi</li>
                <li>Isu-isu penyalahgunaan komputer</li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Poin-poin Penting</h2>
              <ul class="list-disc list-inside mb-4">
                <li>
                  <strong>Etika:</strong> Ilmu tentang apa yang baik dan buruk,
                  tentang hak dan kewajiban moral.
                </li>
                <li>
                  <strong>Etika profesi:</strong> Sikap etis yang harus dimiliki
                  oleh setiap profesional sebagai sikap dalam menjalankan
                  tugasnya.
                </li>
                <li>
                  <strong>Prinsip-prinsip etika profesi:</strong> Tanggung
                  jawab, keadilan, otonomi, integritas moral.
                </li>
                <li>
                  <strong>Profesi:</strong> Pekerjaan yang dilakukan untuk
                  menghasilkan nafkah hidup dan mengandalkan suatu bidang
                  keahlian.
                </li>
                <li>
                  <strong>Ciri-ciri profesi:</strong>
                  <ul class="list-disc list-inside ml-6">
                    <li>Memiliki pengetahuan khusus</li>
                    <li>Memiliki standar dan kaidah moral yang tinggi</li>
                    <li>Mengabdi kepada kepentingan masyarakat</li>
                    <li>Terdapat izin untuk menjalankan profesi</li>
                    <li>Dijalankan oleh kaum profesional</li>
                  </ul>
                </li>
                <li>
                  <strong>Ciri-ciri profesional IT:</strong>
                  <ul class="list-disc list-inside ml-6">
                    <li>Terampil dalam menggunakan peralatan IT</li>
                    <li>
                      Berpengalaman dalam menganalisa software, program, atau
                      aplikasi
                    </li>
                    <li>Memiliki disiplin kerja</li>
                    <li>Dapat bekerja sama dengan baik</li>
                    <li>Cepat tanggap atas keluhan masalah dari klien</li>
                    <li>Mampu menerapkan pendekatan disipliner</li>
                  </ul>
                </li>
                <li>
                  <strong>Etika profesi di bidang IT:</strong> Meliputi prinsip
                  atau norma-norma yang berkaitan dengan hubungan profesional
                  dengan klien.
                </li>
                <li>
                  <strong>Etika penggunaan teknologi informasi:</strong> Etika
                  diperlukan untuk memastikan penggunaan teknologi informasi
                  secara bertanggung jawab dan bermoral.
                </li>
                <li>
                  <strong>Isu-isu penyalahgunaan komputer:</strong> Privasi,
                  akurasi, properti, aksesibilitas.
                </li>
              </ul>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Etika dan profesionalisme penting dalam bidang IT untuk
                memastikan penggunaan teknologi informasi secara bertanggung
                jawab dan bermoral. Ada berbagai prinsip dan norma yang harus
                dipatuhi oleh profesional IT, seperti tanggung jawab, keadilan,
                otonomi, dan integritas moral. Penggunaan teknologi informasi
                juga harus mempertimbangkan privasi, akurasi, properti, dan
                aksesibilitas.
              </p>
            </section>
          </div>
        </div>
        <h2 id="accordion-color-heading-14">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-color-body-14"
            aria-expanded="false"
            aria-controls="accordion-color-body-14"
          >
            <span>Pertemuan 14</span>
            <svg
              data-accordion-icon
              class="w-3 h-3 rotate-180 shrink-0"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5 5 1 1 5"
              />
            </svg>
          </button>
        </h2>
        <div
          id="accordion-color-body-14"
          class="hidden"
          aria-labelledby="accordion-color-heading-14"
        >
          <div class="p-5 border border-gray-200 dark:border-gray-700">
            <section>
              <h2 class="text-xl font-semibold mb-2">
                Pentingnya Etika dalam Penggunaan Komputer
              </h2>
              <p class="mb-4">
                Etika dalam penggunaan komputer penting untuk menjaga
                keseimbangan dalam kehidupan bersama, terutama dengan adanya
                kemajuan teknologi digital dan sosial media.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Perbedaan antara Moral, Etika, dan Hukum
              </h2>
              <p class="mb-4">
                Dibahas mengenai perbedaan antara moral, etika, dan hukum, serta
                pentingnya budaya dan etika dalam lingkup pekerjaan.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Peran Manajer, Karyawan, dan Perusahaan
              </h2>
              <p class="mb-4">
                Pentingnya peran manajer, karyawan, dan seluruh perusahaan dalam
                menjaga etika penggunaan komputer.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Hak-hak Sosial Terkait Penggunaan Komputer
              </h2>
              <p class="mb-4">
                Dibahas mengenai hak-hak sosial terkait penggunaan komputer, hak
                paten, hak cipta, dan merek dagang.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Perlunya Kontrak Sosial dalam Jasa Informasi
              </h2>
              <p class="mb-4">
                Pentingnya kontrak sosial dalam jasa informasi untuk menjaga
                penggunaan komputer yang etis.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Contoh Kasus Pelanggaran Etika
              </h2>
              <p class="mb-4">
                Berbagai contoh kasus pelanggaran etika dalam penggunaan
                komputer dibahas dalam materi.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Pedoman Posisi Duduk yang Benar
              </h2>
              <p class="mb-4">
                Dibahas tentang pedoman posisi duduk yang benar saat menggunakan
                komputer untuk menghindari masalah kesehatan.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Isu-isu Terkait dengan Etika Penggunaan Komputer
              </h2>
              <p class="mb-4">
                Berbagai isu terkait dengan etika penggunaan komputer, seperti
                pekerjaan, kesehatan, kontrol, tanggung jawab, dan kesenjangan
                sosial, dibahas dalam materi.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">
                Langkah-langkah dalam Membuat Isu dan Masalah Sosial
              </h2>
              <p class="mb-4">
                Dibahas langkah-langkah dalam membuat isu dan masalah sosial
                terkait penggunaan komputer dan teknologi dalam masyarakat.
              </p>
            </section>

            <section>
              <h2 class="text-xl font-semibold mb-2">Kesimpulan</h2>
              <p class="mb-4">
                Dengan memahami etika penggunaan komputer, masyarakat dapat
                menjaga keseimbangan dan menghindari konflik serta masalah yang
                mungkin timbul akibat penggunaan teknologi yang tidak bijak.
              </p>
            </section>
          </div>
        </div>
      </div>
    </div>

    <div id="kalender" class="kalender mx-auto max-w-3xl py-16">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-base font-semibold leading-7 text-green-500 pt-8">
          Kalender
        </h2>
        <p
          class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl"
        >
          Jadwal Perkuliahan 2023/2024
        </p>
      </div>
      <img class="pt-16" src="/src/assets/kalender.png" alt="" />
    </div>

    <footer
      class="inset-x-0 bottom-0 z-50 border-t-[1px] border-green-200 bg-green-50"
    >
      <div class="mx-auto max-w-screen-xl px-4 py-8 sm:px-6 lg:px-8">
        <div class="sm:flex sm:items-center sm:justify-between">
          <div class="flex justify-center text-teal-600 sm:justify-start">
            <img class="w-8 h-8" src="@/assets/hzsign.svg" alt="" />
          </div>

          <p
            class="mt-4 text-center text-sm text-gray-500 lg:mt-0 lg:text-right"
          >
            Copyright &copy; Hz Sign 2023. All rights reserved.
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
import ScrollReveal from "scrollreveal";
import { Dialog, DialogPanel } from "@headlessui/vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";
import { initFlowbite } from "flowbite";

onMounted(() => {
  initFlowbite();
});

const navigation = [
  { name: "Profil", href: "#" },
  { name: "Mata Kuliah", href: "#mata-kuliah" },
  { name: "Kalender", href: "#kalender" },
];

const mobileMenuOpen = ref(false);

onMounted(() => {
  ScrollReveal().reveal("header", {
    delay: 500,
  });

  ScrollReveal().reveal(".profil", {
    delay: 500,
    reset: true,
    origin: "bottom",
  });
  ScrollReveal().reveal(".mata-kuliah", {
    delay: 500,
    reset: true,
    origin: "bottom",
  });
  ScrollReveal().reveal(".rangkuman", {
    delay: 500,
    reset: true,
    origin: "bottom",
  });
  ScrollReveal().reveal(".kalender", {
    delay: 500,
    reset: false,
    origin: "bottom",
  });

  ScrollReveal().reveal("nav", {
    delay: 500,
    origin: "top",
  });
});
</script>
