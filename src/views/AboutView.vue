<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'HTML',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png',
          status: 'Intermediate'
        },
        {
          id: 2,
          name: 'CSS',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png',
          status: 'Intermediate'
        },
        {
          id: 3,
          name: 'Angular',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/21_Angular_logo_logos-512.png',
          status: 'Intermediate'
        },
        {
          id: 4,
          name: 'Typescript',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968381.png',
          status: 'Intermediate'
        },
        {
          id: 5,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'Intermediate'
        },    
        {
          id: 6,
          name: 'Vue',
          imageUrl: 'https://images.icon-icons.com/2107/PNG/512/file_type_vue_icon_130078.png',
          status: 'Intermediate'
        },  
        {
          id: 7,
          name: 'Golang',
          imageUrl: 'https://go.dev/blog/go-brand/Go-Logo/PNG/Go-Logo_Blue.png',
          status: 'Intermediate'
        },        
        {
          id: 8,
          name: 'PHP',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png',
          status: 'Intermediate'
        },
        {
          id: 9,
          name: 'Java',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/181_Java_logo_logos-512.png',
          status: 'Intermediate'
        },
        {
          id: 10,
          name: 'Python',
          imageUrl: 'https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png',
          status: 'Beginner'
        },
        {
          id: 11,
          name: 'Laravel',
          imageUrl: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          status: 'Beginner'
        },
        {
          id: 12,
          name: 'Bootstrap',
          imageUrl: 'https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png',
          status: 'Beginner'
        },
      ],
      tools: [
        {
          id: 1,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: 'Version Control'
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://img.icons8.com/m_sharp/200/FFFFFF/github.png',
          status: 'Project List'
        },
        {
          id: 3,
          name: 'VS Code',
          imageUrl: 'https://icons.veryicon.com/png/o/business/vscode-program-item-icon/vscode.png',
          status: 'Code Writting'
        },
        {
          id: 4,
          name: 'Figma',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/a/ad/Figma-1-logo.png',
          status: 'Design'
        },
      ]
    };
  }
}
</script>
<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-teal-50 mx-3 mb-5">
    <article data-page="about">

      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[1px] w-32 bg-teal-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up"
            src="https://i1.sndcdn.com/avatars-000214125831-5q6tdw-t500x500.jpg" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Hello! I’m <strong>Febryan Riyadi</strong>, a 6th-semester Computer Science student at 
            <strong>BINUS University</strong>, Indonesia, majoring in <strong>Software Engineering</strong>. I'm currently working as a 
            <strong>Front-End Developer Intern</strong> at <strong>Periksa.ID</strong>, where I’m actively involved in building and optimizing web applications.
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; I specialize in <strong>front-end development</strong> and <strong>website design</strong>, with a passion for creating clean, 
            responsive, and user-focused interfaces. I believe that great web design blends functionality and aesthetics—resulting in an engaging experience for users.
          </p>
          <p class="mb-3 fadein-left fadeins-3">
            &nbsp; &nbsp; &nbsp; My tech stack includes <strong>Angular</strong>, <strong>TypeScript</strong>, <strong>React</strong>, <strong>Vue</strong>, 
            <strong>HTML</strong>, <strong>CSS</strong>, and <strong>JavaScript</strong>. I strive to continuously improve and grow as a developer—crafting web 
            experiences that not only look good but also perform seamlessly.
          </p>
        </div>
      </section>


    </article>
  </div>

  <div class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-teal-50 mx-3 mb-5">
    <article data-page="education">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          Education &nbsp;
        </div>
      </header>

      <section class="text-sm md:text-lg flex flex-col gap-6">
        <div class="bg-[#2a2a2b] border border-[#383838] rounded-xl p-4 md:p-6 fadein-left fadeins-1">
          <div class="flex flex-col md:flex-row md:justify-between md:items-start mb-3">
            <h3 class="text-lg md:text-xl font-semibold text-teal-200">Natural Science Major</h3>
            <span class="text-sm md:text-base text-gray-400">2019 - 2022</span>
          </div>
          <p class="text-base font-medium text-white mb-2">St. Aloysius 2, Indonesia</p>
          <p class="text-gray-300">
            Completed high school with a focus on Science major, building strong foundation in mathematics, physics, 
            and logical thinking that supports my current studies in Computer Science.
          </p>
        </div>

        <div class="bg-[#2a2a2b] border border-[#383838] rounded-xl p-4 md:p-6 fadein-left fadeins-2">
          <div class="flex flex-col md:flex-row md:justify-between md:items-start mb-3">
            <h3 class="text-lg md:text-xl font-semibold text-teal-200">Undergraduate of Computer Science</h3>
            <span class="text-sm md:text-base text-gray-400">2022 - 2026 (expected)</span>
          </div>
          <p class="text-base font-medium text-white mb-2">BINUS University, Indonesia</p>
          <p class="text-gray-300">
            Currently pursuing a Bachelor's degree in Computer Science with focus on software engineering and web development. 
            Gaining comprehensive knowledge in programming fundamentals, data structures, algorithms, and modern web technologies.
          </p>
        </div>
      </section>
    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-teal-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-teal-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-teal-200 bg-teal-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech Stack</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-teal-200 bg-teal-200 bg-opacity-10': activeTab === 2 }" @click="activeTab = 2">Tools</button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-teal-200 px-2 py-2 hover:bg-teal-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-teal-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-teal-200 px-2 py-2 hover:bg-teal-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-teal-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}
</style>
