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
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:text-center">
          <h2 class="text-base font-semibold leading-7 text-green-500">
            Mata Kuliah
          </h2>
          <p
            class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl"
          >
            Catatan Rangkuman Perkuliahan
          </p>
        </div>
      </div>

      <div
        id="accordion-nested-parent"
        data-accordion="collapse"
        class="py-8 px-8 pb-32 text-left"
      >
        <h2 id="accordion-collapse-heading-1">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 rounded-t-xl focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-1"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-1"
          >
            <span>Bahasa Indonesia</span>
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
          id="accordion-collapse-body-1"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-1"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div id="accordion-nested-collapse" data-accordion="collapse">
              <h2 id="accordion-nested-collapse-heading-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-1"
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
                id="accordion-nested-collapse-body-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Nostrum beatae ipsam exercitationem ratione accusantium
                    atque commodi, necessitatibus tempora error quia, accusamus
                    officiis quo alias assumenda dignissimos! Dolorem sed
                    delectus ipsum.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-2"
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
                id="accordion-nested-collapse-body-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Veniam laudantium unde quod nemo magni, sed veritatis sunt
                    animi pariatur iusto, illum voluptatum. Assumenda
                    consectetur odit laborum reprehenderit illum quis ipsum.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-3"
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
                id="accordion-nested-collapse-body-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Unde sunt molestias veritatis eveniet ullam repellendus
                    minima earum, libero sequi. Quo nam molestias exercitationem
                    aspernatur! Suscipit sint cupiditate eligendi nobis
                    recusandae.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-2">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-2"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-2"
          >
            <span>Intermediate Academic English</span>
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
          id="accordion-collapse-body-2"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-2"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div
              id="accordion-nested-collapse-english-1"
              data-accordion="collapse"
            >
              <h2 id="accordion-nested-collapse-heading-english-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-english-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-english-1"
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
                id="accordion-nested-collapse-body-english-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-english-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-english-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-english-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-english-2"
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
                id="accordion-nested-collapse-body-english-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-english-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-english-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-english-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-english-3"
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
                id="accordion-nested-collapse-body-english-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-english-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-3">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-3"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-3"
          >
            <span>Komputer dan Masyarakat</span>
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
          id="accordion-collapse-body-3"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-3"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div
              id="accordion-nested-collapse-komnas-1"
              data-accordion="collapse"
            >
              <h2 id="accordion-nested-collapse-heading-komnas-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komnas-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komnas-1"
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
                id="accordion-nested-collapse-body-komnas-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komnas-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-komnas-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komnas-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komnas-2"
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
                id="accordion-nested-collapse-body-komnas-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komnas-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-komnas-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komnas-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komnas-3"
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
                id="accordion-nested-collapse-body-komnas-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komnas-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-4">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-4"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-4"
          >
            <span>Komputer Grafik</span>
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
          id="accordion-collapse-body-4"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-4"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div
              id="accordion-nested-collapse-komgraf-1"
              data-accordion="collapse"
            >
              <h2 id="accordion-nested-collapse-heading-komgraf-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komgraf-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komgraf-1"
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
                id="accordion-nested-collapse-body-komgraf-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komgraf-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-komgraf-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komgraf-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komgraf-2"
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
                id="accordion-nested-collapse-body-komgraf-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komgraf-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-komgraf-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komgraf-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komgraf-3"
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
                id="accordion-nested-collapse-body-komgraf-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komgraf-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-5">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-5"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-5"
          >
            <span>Sistem Operasi</span>
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
          id="accordion-collapse-body-5"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-5"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div
              id="accordion-nested-collapse-sisop-1"
              data-accordion="collapse"
            >
              <h2 id="accordion-nested-collapse-heading-sisop-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-sisop-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-sisop-1"
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
                id="accordion-nested-collapse-body-sisop-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-sisop-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-sisop-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-sisop-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-sisop-2"
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
                id="accordion-nested-collapse-body-sisop-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-sisop-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-sisop-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-sisop-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-sisop-3"
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
                id="accordion-nested-collapse-body-sisop-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-sisop-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-6">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-6"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-6"
          >
            <span>Pengantar Aplikasi Komputer</span>
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
          id="accordion-collapse-body-6"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-6"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div id="accordion-nested-collapse-pak-1" data-accordion="collapse">
              <h2 id="accordion-nested-collapse-heading-pak-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-pak-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-pak-1"
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
                id="accordion-nested-collapse-body-pak-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-pak-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-pak-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-pak-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-pak-2"
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
                id="accordion-nested-collapse-body-pak-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-pak-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-pak-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-pak-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-pak-3"
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
                id="accordion-nested-collapse-body-pak-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-pak-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-7">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-7"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-7"
          >
            <span>Komukasi Data</span>
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
          id="accordion-collapse-body-7"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-7"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div
              id="accordion-nested-collapse-komdat-1"
              data-accordion="collapse"
            >
              <h2 id="accordion-nested-collapse-heading-komdat-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komdat-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komdat-1"
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
                id="accordion-nested-collapse-body-komdat-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komdat-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-komdat-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komdat-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komdat-2"
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
                id="accordion-nested-collapse-body-komdat-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komdat-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-komdat-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-komdat-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-komdat-3"
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
                id="accordion-nested-collapse-body-komdat-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-komdat-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-8">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-8"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-8"
          >
            <span>Kalkulus II</span>
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
          id="accordion-collapse-body-8"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-8"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div id="accordion-nested-collapse-kal-1" data-accordion="collapse">
              <h2 id="accordion-nested-collapse-heading-kal-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-kal-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-kal-1"
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
                id="accordion-nested-collapse-body-kal-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-kal-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-kal-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-kal-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-kal-2"
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
                id="accordion-nested-collapse-body-kal-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-kal-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-kal-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-kal-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-kal-3"
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
                id="accordion-nested-collapse-body-kal-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-kal-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
        <h2 id="accordion-collapse-heading-9">
          <button
            type="button"
            class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-t-b-0 border-gray-200 rounded-b-xl focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
            data-accordion-target="#accordion-collapse-body-9"
            aria-expanded="true"
            aria-controls="accordion-collapse-body-9"
          >
            <span>Pendidikan Kewarganegaraan</span>
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
          id="accordion-collapse-body-9"
          class="hidden"
          aria-labelledby="accordion-collapse-heading-9"
        >
          <div
            class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900"
          >
            <!-- Nested accordion -->
            <div id="accordion-nested-collapse-pkn-1" data-accordion="collapse">
              <h2 id="accordion-nested-collapse-heading-pkn-1">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 rounded-t-xl font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-pkn-1"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-pkn-1"
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
                id="accordion-nested-collapse-body-pkn-1"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-pkn-1"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Exercitationem suscipit molestiae voluptate ut cupiditate
                    necessitatibus quaerat reiciendis, dolores et dicta dolor a
                    praesentium impedit minima magnam mollitia repellat in
                    consequuntur?
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-pkn-2">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-pkn-2"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-pkn-2"
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
                id="accordion-nested-collapse-body-pkn-2"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-pkn-2"
              >
                <div
                  class="p-5 border border-b-0 border-gray-200 dark:border-gray-700"
                >
                  <p class="text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Tenetur placeat aperiam, praesentium pariatur accusamus
                    deleniti. Optio beatae eligendi adipisci nulla eum,
                    perferendis veniam. Fugit quisquam totam minus repellat
                    porro sed.
                  </p>
                </div>
              </div>
              <h2 id="accordion-nested-collapse-heading-pkn-3">
                <button
                  type="button"
                  class="flex items-center justify-between w-full p-5 font-medium rtl:text-right text-gray-500 border border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 gap-3"
                  data-accordion-target="#accordion-nested-collapse-body-pkn-3"
                  aria-expanded="false"
                  aria-controls="accordion-nested-collapse-body-pkn-3"
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
                id="accordion-nested-collapse-body-pkn-3"
                class="hidden"
                aria-labelledby="accordion-nested-collapse-heading-pkn-3"
              >
                <div class="p-5 border border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    We actually recommend using both Flowbite, Flowbite Pro, and
                    even Tailwind UI as there is no technical reason stopping
                    you from using the best of two worlds.
                  </p>
                </div>
              </div>
            </div>
            <!-- End: Nested accordion -->
          </div>
        </div>
      </div>
    </div>

    <div
      id="kalender"
      class="kalender mx-auto max-w-3xl py-16 sm:py-16 lg:py-24"
    >
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-base font-semibold leading-7 text-green-500">
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
    reset: true,
    origin: "bottom",
  });

  ScrollReveal().reveal("nav", {
    delay: 500,
    origin: "top",
  });
});
</script>
