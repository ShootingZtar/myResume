<script setup>
const profile = {
  name: 'Kanisorn Lee',
  title: 'Full-Stack Developer',
  email: 'devzero.lee@email.com',
  phone: '+66 85-035-3543',
  location: 'Chiang Mai, Thailand',
  linkedin: 'linkedin.com/in/kanisorn-lee/',
  github: 'github.com/ShootingZtar',
  summary:
    'Experienced full-stack developer with 5+ years building scalable web and mobile applications. Passionate about clean architecture, developer experience, and delivering high-quality products. Skilled in modern JavaScript/TypeScript ecosystems and mobile development with a strong foundation in cloud infrastructure.',
}

const experiences = [
  {
    role: 'Software Developer',
    company: 'Odd-e Co., Ltd.',
    period: 'Feb 2021 — Present',
    highlights: [
      'Designed and implemented microservices architecture handling 100K+ requests/sec',
      'Developed mobile applications using Flutter',
      'Developed web applications using Angular for the frontend and Go for the backend',
      'Established CI/CD pipelines with GitLab pipelines with GCP as a cloud infrastructure',
    ],
  },
  {
    role: 'Software Developer',
    company: 'ITSC of Chiang Mai University',
    period: 'May 2016 — Dec 2021',
    highlights: [
      'Built web application for real-time dashboard, mobile application for students',
      'Developed RESTful APIs with Node.js and PostgreSQL serving 50K daily active users',
      'Developed web application for Leave Application form for officers',
      'Mentored 2 junior developers and conducted code reviews',
    ],
  },
]

const education = [
  {
    degree: 'Bachelor of Science in Computer Science',
    school: 'Chiang Mai Rajabhat University',
    period: '2010 — 2014',
    detail: 'GPA 3.12',
  },
]

const skills = {
  Frontend: ['Vue.js', 'Nuxt', 'React', 'TypeScript', 'Tailwind CSS', 'Bootstrap', 'Vuetify'],
  Backend: ['Node.js', 'Go', 'PostgreSQL', 'Redis', 'GraphQL'],
  DevOps: ['Docker', 'GCP', 'AWS', 'GitHub Actions', 'Terraform'],
  Tools: ['Git', 'Figma', 'Jira', 'VS Code', 'Cursor', 'Postman', 'Bruno'],
}

const languages = [
  { name: 'Thai', level: 'Native' },
  { name: 'English', level: 'Professional' },
  { name: 'Japanese', level: 'Basic' },
  { name: 'Chinese', level: 'Basic' },
]

function handlePrint() {
  window.print()
}
</script>

<template>
  <div class="min-h-screen bg-gray-100 font-[Inter,sans-serif] print:bg-white print:min-h-0">
    <!-- Print Button -->
    <div class="fixed bottom-6 right-6 z-50 print-hidden">
      <button @click="handlePrint"
        class="flex items-center gap-2 bg-slate-800 hover:bg-slate-700 text-white px-5 py-3 rounded-full shadow-lg cursor-pointer transition-colors">
        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"
          stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round"
            d="M17 17h2a2 2 0 002-2v-4a2 2 0 00-2-2H5a2 2 0 00-2 2v4a2 2 0 002 2h2m2 4h6a2 2 0 002-2v-4a2 2 0 00-2-2H9a2 2 0 00-2 2v4a2 2 0 002 2zm8-12V5a2 2 0 00-2-2H9a2 2 0 00-2 2v4h10z" />
        </svg>
        Print CV
      </button>
    </div>

    <!-- CV Page -->
    <div class="max-w-[210mm] mx-auto bg-white shadow-xl print:shadow-none print:mx-0">
      <div
        class="grid grid-cols-1 md:grid-cols-[280px_1fr] print:grid-cols-[200px_1fr] min-h-screen print:min-h-0 print:h-[297mm]">

        <!-- Sidebar -->
        <aside class="bg-slate-800 text-white p-6 print:p-5 print:text-[10px]">
          <!-- Avatar -->
          <!-- <div class="flex justify-center mb-5">
            <div
              class="w-28 h-28 print:w-20 print:h-20 rounded-full bg-slate-600 flex items-center justify-center text-4xl print:text-2xl font-bold text-slate-200 ring-4 ring-slate-500">
              {{profile.name.split(' ').map(n => n[0]).join('')}}
            </div>
          </div> -->

          <!-- Contact -->
          <div class="mb-6 print:mb-4">
            <h2 class="text-xs font-bold uppercase tracking-widest text-slate-400 mb-3 print:mb-2 print:text-[9px]">
              Contact</h2>
            <ul class="space-y-2 print:space-y-1 text-sm print:text-[10px]">
              <li class="flex items-start gap-2">
                <svg class="w-4 h-4 mt-0.5 shrink-0 text-slate-400" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
                <span class="break-all">{{ profile.email }}</span>
              </li>
              <li class="flex items-start gap-2">
                <svg class="w-4 h-4 mt-0.5 shrink-0 text-slate-400" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
                <span>{{ profile.phone }}</span>
              </li>
              <li class="flex items-start gap-2">
                <svg class="w-4 h-4 mt-0.5 shrink-0 text-slate-400" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                <span>{{ profile.location }}</span>
              </li>
              <li class="flex items-start gap-2">
                <svg class="w-4 h-4 mt-0.5 shrink-0 text-slate-400" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
                </svg>
                <span>{{ profile.linkedin }}</span>
              </li>
              <li class="flex items-start gap-2">
                <svg class="w-4 h-4 mt-0.5 shrink-0 text-slate-400" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
                </svg>
                <span>{{ profile.github }}</span>
              </li>
            </ul>
          </div>

          <!-- Skills -->
          <div class="mb-6 print:mb-4">
            <h2 class="text-xs font-bold uppercase tracking-widest text-slate-400 mb-3 print:mb-2 print:text-[9px]">
              Skills</h2>
            <div class="space-y-3 print:space-y-2">
              <div v-for="(items, category) in skills" :key="category">
                <h3 class="text-sm print:text-[10px] font-semibold text-slate-300 mb-1.5 print:mb-1">{{ category }}</h3>
                <div class="flex flex-wrap gap-1.5 print:gap-1">
                  <span v-for="skill in items" :key="skill"
                    class="px-2 py-0.5 bg-slate-700 rounded text-xs print:text-[9px] text-slate-300">
                    {{ skill }}
                  </span>
                </div>
              </div>
            </div>
          </div>

          <!-- Languages -->
          <div>
            <h2 class="text-xs font-bold uppercase tracking-widest text-slate-400 mb-3 print:mb-2 print:text-[9px]">
              Languages</h2>
            <ul class="space-y-1 text-sm print:text-[10px]">
              <li v-for="lang in languages" :key="lang.name" class="flex justify-between">
                <span>{{ lang.name }}</span>
                <span class="text-slate-400">{{ lang.level }}</span>
              </li>
            </ul>
          </div>
        </aside>

        <!-- Main Content -->
        <main class="p-6 md:p-8 print:p-5 print:text-[10px]">
          <!-- Header -->
          <header class="mb-6 print:mb-4">
            <h1 class="text-3xl md:text-4xl print:text-2xl font-bold text-slate-800 leading-tight">
              {{ profile.name }}
            </h1>
            <p class="text-lg print:text-sm font-medium text-blue-600 mt-1">
              {{ profile.title }}
            </p>
            <p class="text-sm print:text-[10px] text-slate-600 mt-3 print:mt-2 leading-relaxed">
              {{ profile.summary }}
            </p>
          </header>

          <hr class="border-slate-200 mb-6 print:mb-4" />

          <!-- Experience -->
          <section class="mb-6 print:mb-4">
            <h2 class="text-sm font-bold uppercase tracking-widest text-slate-400 mb-4 print:mb-2 print:text-[9px]">
              Work Experience
            </h2>
            <div class="space-y-5 print:space-y-3">
              <div v-for="exp in experiences" :key="exp.company">
                <div class="flex flex-col sm:flex-row sm:items-baseline sm:justify-between gap-0.5 mb-1.5 print:mb-1">
                  <div>
                    <h3 class="text-base print:text-[11px] font-semibold text-slate-800">{{ exp.role }}</h3>
                    <p class="text-sm print:text-[10px] text-blue-600 font-medium">{{ exp.company }}</p>
                  </div>
                  <span class="text-xs print:text-[9px] text-slate-400 whitespace-nowrap">{{ exp.period }}</span>
                </div>
                <ul class="space-y-1 print:space-y-0.5">
                  <li v-for="(h, i) in exp.highlights" :key="i"
                    class="text-sm print:text-[10px] text-slate-600 leading-relaxed pl-4 relative before:content-['•'] before:absolute before:left-0 before:text-slate-400">
                    {{ h }}
                  </li>
                </ul>
              </div>
            </div>
          </section>

          <hr class="border-slate-200 mb-6 print:mb-4" />

          <!-- Education -->
          <section>
            <h2 class="text-sm font-bold uppercase tracking-widest text-slate-400 mb-4 print:mb-2 print:text-[9px]">
              Education
            </h2>
            <div v-for="edu in education" :key="edu.school">
              <div class="flex flex-col sm:flex-row sm:items-baseline sm:justify-between gap-0.5 mb-1 print:mb-0.5">
                <div>
                  <h3 class="text-base print:text-[11px] font-semibold text-slate-800">{{ edu.degree }}</h3>
                  <p class="text-sm print:text-[10px] text-blue-600 font-medium">{{ edu.school }}</p>
                </div>
                <span class="text-xs print:text-[9px] text-slate-400 whitespace-nowrap">{{ edu.period }}</span>
              </div>
              <p class="text-sm print:text-[10px] text-slate-600">{{ edu.detail }}</p>
            </div>
          </section>
        </main>
      </div>
    </div>
  </div>
</template>
