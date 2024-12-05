<template>
  <header
    class="lg:sticky lg:top-0 lg:flex lg:max-h-screen lg:w-1/3 lg:flex-col lg:justify-between lg:py-24">
    <div>
      <h1 class="text-4xl font-bold tracking-tight text-slate-200 sm:text-5xl">
        Seda Genc
      </h1>
      <h2
        class="mt-2 text-lg font-medium tracking-tight text-slate-200 sm:text-xl">
        Industrial Engineer
      </h2>
      <p class="mt-3 max-w-xs leading-normal">
        I like solving problems through programming and building things that
        help people.
      </p>
      <a
        class="mt-2 group/korok inline-flex lg:font-medium text-slate-200"
        href="./sedagenc_cv.pdf"
        download
        target="_blank">
        <span class="sr-only">Download my CV</span>
        <span
          class="group-hover/korok:text-red-400 transition duration-75 group-hover/korok:-translate-y-px delay-[50ms]"
          aria-hidden="true">
          D
        </span>
        <span
          class="group-hover/korok:text-orange-400 transition duration-75 group-hover/korok:-translate-y-px delay-[75ms]"
          aria-hidden="true">
          o
        </span>
        <span
          class="group-hover/korok:text-yellow-400 transition duration-75 group-hover/korok:-translate-y-px delay-[100ms]"
          aria-hidden="true">
          w
        </span>
        <span
          class="group-hover/korok:text-lime-400 transition duration-75 group-hover/korok:-translate-y-px delay-[125ms]"
          aria-hidden="true">
          n
        </span>
        <span
          class="group-hover/korok:text-green-400 transition duration-75 group-hover/korok:-translate-y-px delay-[150ms]"
          aria-hidden="true">
          l
        </span>
        <span
          class="group-hover/korok:text-teal-400 transition duration-75 group-hover/korok:-translate-y-px delay-[175ms]"
          aria-hidden="true">
          o
        </span>
        <span
          class="group-hover/korok:text-cyan-400 transition duration-75 group-hover/korok:-translate-y-px delay-[200ms]"
          aria-hidden="true">
          a
        </span>
        <span
          class="group-hover/korok:text-sky-400 transition duration-75 group-hover/korok:-translate-y-px delay-[225ms]"
          aria-hidden="true">
          d
        </span>
        <span
          class="group-hover/korok:text-blue-400 transition duration-75 group-hover/korok:-translate-y-px delay-[250ms]"
          aria-hidden="true">
          &nbsp;
        </span>
        <span
          class="group-hover/korok:text-indigo-400 transition duration-75 group-hover/korok:-translate-y-px delay-[275ms]"
          aria-hidden="true">
          m
        </span>
        <span
          class="group-hover/korok:text-violet-400 transition duration-75 group-hover/korok:-translate-y-px delay-[300ms]"
          aria-hidden="true">
          y
        </span>
        <span
          class="group-hover/korok:text-pink-400 transition duration-75 group-hover/korok:-translate-y-px delay-[325ms]"
          aria-hidden="true">
          &nbsp;
        </span>
        <span
          class="group-hover/korok:text-red-400 transition duration-75 group-hover/korok:-translate-y-px delay-[350ms]"
          aria-hidden="true">
          C
        </span>
        <span
          class="group-hover/korok:text-orange-400 transition duration-75 group-hover/korok:-translate-y-px delay-[375ms]"
          aria-hidden="true">
          V
        </span>

        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 group-hover/korok:text-yellow-400 transition duration-75 group-hover/korok:-translate-y-px delay-[425ms]"
          fill="currentColor"
          viewBox="0 0 24 24"
          aria-hidden="true">
          <path d="M12 16l4-5h-3V4h-2v7H8l4 5zm-7 4h14v-2H5v2z" />
        </svg>
      </a>
      <nav class="nav hidden lg:block" aria-label="In-page jump links">
        <ul class="mt-12 w-max">
          <li>
            <a
              :class="[
                'group flex items-center py-3',
                { active: activeSection === 'about' },
              ]"
              href="/personal-page/?view=main#about">
              <!-- Dynamic Indicator -->
              <span
                :class="[
                  'nav-indicator mr-4 h-px w-8 transition-all motion-reduce:transition-none',
                  {
                    'w-16 bg-slate-200': activeSection === 'about', // When active
                    'group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 bg-slate-600':
                      activeSection !== 'about',
                  },
                ]">
              </span>

              <!-- Dynamic Text -->
              <span
                :class="[
                  'nav-text text-xs font-bold uppercase tracking-widest transition-all',
                  {
                    'text-slate-200': activeSection === 'about', // Text color when active
                    'text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200':
                      activeSection !== 'about',
                  },
                ]">
                About
              </span>
            </a>
          </li>
          <li>
            <a
              :class="[
                'group flex items-center py-3',
                { active: activeSection === 'experience' },
              ]"
              href="/personal-page/?view=main#experience">
              <!-- Dynamic Indicator -->
              <span
                :class="[
                  'nav-indicator mr-4 h-px w-8 transition-all motion-reduce:transition-none',
                  {
                    'w-16 bg-slate-200': activeSection === 'experience', // When active
                    'group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 bg-slate-600':
                      activeSection !== 'experience',
                  },
                ]">
              </span>

              <!-- Dynamic Text -->
              <span
                :class="[
                  'nav-text text-xs font-bold uppercase tracking-widest transition-all',
                  {
                    'text-slate-200': activeSection === 'experience', // Text color when active
                    'text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200':
                      activeSection !== 'experience',
                  },
                ]">
                Experience
              </span>
            </a>
          </li>
          <li>
            <a
              :class="[
                'group flex items-center py-3',
                { active: activeSection === 'projects' },
              ]"
              href="/personal-page/?view=main#projects">
              <!-- Dynamic Indicator -->
              <span
                :class="[
                  'nav-indicator mr-4 h-px w-8 transition-all motion-reduce:transition-none',
                  {
                    'w-16 bg-slate-200': activeSection === 'projects', // When active
                    'group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 bg-slate-600':
                      activeSection !== 'projects',
                  },
                ]">
              </span>

              <!-- Dynamic Text -->
              <span
                :class="[
                  'nav-text text-xs font-bold uppercase tracking-widest transition-all',
                  {
                    'text-slate-200': activeSection === 'projects', // Text color when active
                    'text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200':
                      activeSection !== 'projects',
                  },
                ]">
                Projects
              </span>
            </a>
          </li>
        </ul>
      </nav>
    </div>
    <ul class="ml-1 mt-8 flex-col items-center" aria-label="Social media">
      <li class="mr-5 shrink-0 text-xs">
        <p class="mt-4 max-w-xs leading-normal">+90 531 917 83 74</p>
      </li>
      <li class="mr-5 shrink-0 text-xs">
        <p class="mt-4 max-w-xs leading-normal">seedagenc@gmail.com</p>
      </li>
    </ul>
    <ul class="ml-1 mt-4 flex items-center" aria-label="Social media">
      <li class="mr-5 shrink-0 text-xs">
        <a
          class="block hover:text-slate-200"
          href="https://www.linkedin.com/in/seedagenc/"
          target="_blank"
          rel="noreferrer noopener"
          aria-label="LinkedIn (opens in a new tab)"
          title="LinkedIn"
          ><span class="sr-only">LinkedIn</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="h-6 w-6"
            aria-hidden="true">
            <path
              d="M20.5 2h-17A1.5 1.5 0 002 3.5v17A1.5 1.5 0 003.5 22h17a1.5 1.5 0 001.5-1.5v-17A1.5 1.5 0 0020.5 2zM8 19H5v-9h3zM6.5 8.25A1.75 1.75 0 118.3 6.5a1.78 1.78 0 01-1.8 1.75zM19 19h-3v-4.74c0-1.42-.6-1.93-1.38-1.93A1.74 1.74 0 0013 14.19a.66.66 0 000 .14V19h-3v-9h2.9v1.3a3.11 3.11 0 012.7-1.4c1.55 0 3.36.86 3.36 3.66z"></path></svg
        ></a>
      </li>

      <li class="mr-5 shrink-0 text-xs">
        <a
          class="block hover:text-slate-200"
          href="https://www.instagram.com/poinedaa/"
          target="_blank"
          rel="noreferrer noopener"
          aria-label="Goodreads (opens in a new tab)"
          title="Goodreads">
          <span class="sr-only">Goodreads</span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-instagram"
            viewBox="0 0 16 16">
            <path
              d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.9 3.9 0 0 0-1.417.923A3.9 3.9 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.9 3.9 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.9 3.9 0 0 0-.923-1.417A3.9 3.9 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599s.453.546.598.92c.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.5 2.5 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.5 2.5 0 0 1-.92-.598 2.5 2.5 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233s.008-2.388.046-3.231c.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92s.546-.453.92-.598c.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92m-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217m0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334" />
          </svg>
        </a>
      </li>
    </ul>
  </header>
</template>

<script setup>
const props = defineProps({
  activeSection: String,
});
</script>
