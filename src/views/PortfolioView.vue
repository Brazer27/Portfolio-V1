<script>
export default {
  data() {
    return {
      activeTab: 1,
      projects: [
        {
          id: 1,
          name: 'SEHATI',
          imageUrl: 'sehati',
          status: 'Mental health application that helps users manage their well-being through stress assessments and informative articles.',
          tech: 'PHP, Blade',
          github: 'https://github.com/Brazer27/Project-Software-Enginering',
          demo: 'null'
        },
        {
          id: 2,
          name: 'GymMe',
          imageUrl: 'gymme',
          status: 'Online platform for purchasing health supplements, allowing users to shop easily and enabling store admins to manage inventory and sales.',
          tech: 'JavaScript, CSS',
          github: 'https://github.com/Brazer27/Project-PSD',
          demo: 'null'
        },
        {
          id: 3,
          name: 'Ceilo',
          imageUrl: 'ceilo',
          status: 'Psychology application that allows users to chat anonymously and consult with professionals, providing a safe space for mental health discussions, along with a forum for community support and interaction.',
          tech: 'Vue, CSS',
          github: 'null',
          demo: 'null'
        },
        {
          id: 4,
          name: 'DigiMed',
          imageUrl: 'digimed',
          status: 'Online health consultation application equipped with AI diagnosis, enabling users to receive medical advice while also offering an online pharmacy feature for convenient access to medications.',
          tech: 'Figma',
          github: 'null',
          demo: 'null'
        }
      ],
      workExperience: [
        {
          id: 1,
          company: 'Periksa.ID',
          role: 'Front End Developer Intern',
          period: 'Feb 2025 - Now',
          description: 'Developed and maintained healthcare management system interfaces using Angular and TypeScript. Collaborated with backend team to integrate Golang APIs and implemented various UI/UX improvements for hospital management modules. Worked on critical healthcare features including patient management, medical records, and administrative systems.',
          technologies: ['Angular', 'TypeScript', 'Golang', 'HTML', 'SCSS', 'JavaScript', 'CSS', 'Git'],
          achievements: [
            'Successfully resolved 35+ critical issues across various hospital management modules',
            'Implemented UI improvements for user profile and medical record management systems',
            'Developed API integrations for multiple healthcare modules using Golang',
            'Enhanced patient management features with advanced filtering and pagination',
            'Contributed to medical documentation systems and report generation features'
          ],
          keyProjects: [
            'Patient Management System UI/UX improvements',
            'Medical Records and Documentation modules',
            'Healthcare API integrations with Golang backend',
            'Hospital administrative systems enhancement',
            'Medical billing and inventory management features'
          ]
        }
      ],
      internshipSummary: {
        title: 'Internship Experience Summary',
        description: 'During my internship at Periksa.ID, I gained valuable hands-on experience in healthcare technology development, working with Angular and TypeScript to build robust medical management systems. I collaborated with cross-functional teams to deliver critical healthcare solutions and contributed to various modules including patient management, medical records, and administrative systems.',
        keyLearnings: [
          'Healthcare software development with Angular and TypeScript',
          'Backend integration using Golang APIs and RESTful services',
          'Agile development methodologies in healthcare technology environment',
          'Medical data management and patient privacy considerations',
          'Cross-platform development and responsive design for healthcare applications',
          'Code review processes and version control in team-based healthcare projects'
        ]
      }
    };
  }
}
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-teal-50 mx-3">
    <article data-page="portfolio">
      <header>
        <div class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Professional Experience</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-teal-300">
            Explore my projects and work experience
          </h4>
        </div>
      </header>
      
      <section>
        <!-- Tab Navigation -->
        <div class="mb-8">
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5 justify-center">
            <li class="mr-2">
              <button class="inline-block px-6 py-3 rounded-lg hover:text-white transition-all duration-200"
                :class="{ 'text-teal-200 bg-teal-200 bg-opacity-10': activeTab === 1 }" 
                @click="activeTab = 1">
                My Projects
              </button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-6 py-3 rounded-lg hover:text-white transition-all duration-200"
                :class="{ 'text-teal-200 bg-teal-200 bg-opacity-10': activeTab === 2 }" 
                @click="activeTab = 2">
                Work Experience
              </button>
            </li>
          </ul>
        </div>

        <!-- My Projects Tab -->
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-1 gap-6 pb-32 md:grid-cols-2 lg:grid-cols-3 xl:gap-8 fade-zoom-in">
            <div v-for="item in projects" :key="item.id">
              <div class="item-card flex flex-col gap-4 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-teal-50 p-6 h-full transition-all duration-300">
                <!-- Project Image -->
                <div class="project-image-container">
                  <img alt="Project Image" 
                       loading="lazy" 
                       decoding="async" 
                       class="project-image drop-shadow-xl rounded-xl w-full h-48 object-cover"
                       :src="'/img/portfolio-' + item.imageUrl + '.png'">
                </div>
                
                <!-- Project Content -->
                <div class="flex flex-col gap-3 flex-grow">
                  <div class="project-title font-bold text-lg text-white">
                    {{ item.name }}
                  </div>
                  
                  <div class="project-description text-sm text-[#c1c1c1] leading-relaxed flex-grow">
                    {{ item.status }}
                  </div>
                  
                  <div class="project-tech text-sm text-teal-200 font-medium">
                    {{ item.tech }}
                  </div>
                  
                  <!-- Project Links -->
                  <div class="flex justify-end gap-3 mt-4">
                    <a v-if="item.github !== 'null'"
                       :href="item.github" 
                       target="_blank" 
                       rel="noreferrer"
                       title="View github repository" 
                       class="project-link transition-all hover:text-teal-200 hover:scale-110">
                      <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" 
                           stroke-linecap="round" stroke-linejoin="round" height="20" width="20" 
                           xmlns="http://www.w3.org/2000/svg">
                        <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                      </svg>
                    </a>
                    
                    <a v-if="item.demo !== 'null'" 
                       :href="item.demo" 
                       target="_blank" 
                       rel="noreferrer"
                       title="View live demo" 
                       class="project-link transition-all hover:text-teal-200 hover:scale-110">
                      <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" 
                           stroke-linecap="round" stroke-linejoin="round" height="20" width="20" 
                           xmlns="http://www.w3.org/2000/svg">
                        <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                        <polyline points="15 3 21 3 21 9"></polyline>
                        <line x1="10" y1="14" x2="21" y2="3"></line>
                      </svg>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Work Experience Tab -->
        <div v-show="activeTab === 2">
          <!-- Internship Summary -->
          <div class="mb-12">
            <div class="bg-[#1e1e1f] border border-[#383838] rounded-xl p-8 mb-8">
              <h3 class="text-xl font-bold text-white mb-4">{{ internshipSummary.title }}</h3>
              <p class="text-[#c1c1c1] mb-6 leading-relaxed">{{ internshipSummary.description }}</p>
              
              <h4 class="text-lg font-semibold text-teal-200 mb-3">Key Learnings:</h4>
              <ul class="space-y-2">
                <li v-for="learning in internshipSummary.keyLearnings" :key="learning" 
                    class="flex items-start gap-2 text-[#c1c1c1]">
                  <span class="text-teal-200 mt-1">•</span>
                  <span>{{ learning }}</span>
                </li>
              </ul>
            </div>
          </div>

          <!-- Work Experience Cards -->
          <div class="space-y-8 pb-32">
            <div v-for="work in workExperience" :key="work.id">
              <div class="work-card bg-[#1e1e1f] border border-[#383838] rounded-xl p-8">
                <div class="flex flex-col md:flex-row md:justify-between md:items-start mb-6">
                  <div>
                    <h3 class="text-xl font-bold text-white mb-2">{{ work.role }}</h3>
                    <h4 class="text-lg text-teal-200 font-medium mb-2">{{ work.company }}</h4>
                  </div>
                  <span class="text-sm text-[#c1c1c1] bg-[#383838] px-3 py-1 rounded-full">{{ work.period }}</span>
                </div>
                
                <p class="text-[#c1c1c1] mb-6 leading-relaxed">{{ work.description }}</p>
                
                <div class="mb-6">
                  <h5 class="text-sm font-semibold text-teal-200 mb-3">Technologies Used:</h5>
                  <div class="flex flex-wrap gap-2">
                    <span v-for="tech in work.technologies" :key="tech" 
                          class="bg-teal-200 bg-opacity-10 text-teal-200 px-3 py-1 rounded-full text-sm">
                      {{ tech }}
                    </span>
                  </div>
                </div>

                <!-- Project Statistics (if available) -->
                <div v-if="work.projectStats" class="mb-6">
                  <h5 class="text-sm font-semibold text-teal-200 mb-3">Project Language Distribution:</h5>
                  <div class="grid grid-cols-2 md:grid-cols-3 gap-3">
                    <div v-for="(percentage, language) in work.projectStats" :key="language" 
                         class="bg-[#383838] rounded-lg p-3 text-center">
                      <div class="text-white font-medium text-sm">{{ language }}</div>
                      <div class="text-teal-200 text-xs">{{ percentage }}</div>
                    </div>
                  </div>
                </div>

                <!-- Key Projects (if available) -->
                <div v-if="work.keyProjects" class="mb-6">
                  <h5 class="text-sm font-semibold text-teal-200 mb-3">Key Projects:</h5>
                  <ul class="space-y-2">
                    <li v-for="project in work.keyProjects" :key="project" 
                        class="flex items-start gap-2 text-[#c1c1c1]">
                      <span class="text-teal-200 mt-1">→</span>
                      <span>{{ project }}</span>
                    </li>
                  </ul>
                </div>
                
                <div>
                  <h5 class="text-sm font-semibold text-teal-200 mb-3">Key Achievements:</h5>
                  <ul class="space-y-2">
                    <li v-for="achievement in work.achievements" :key="achievement" 
                        class="flex items-start gap-2 text-[#c1c1c1]">
                      <span class="text-teal-200 mt-1">✓</span>
                      <span>{{ achievement }}</span>
                    </li>
                  </ul>
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
.item-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  min-height: 400px;
}

.item-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.project-image {
  transition: transform 0.3s ease;
}

.item-card:hover .project-image {
  transform: scale(1.05);
}

.project-link {
  color: #94a3b8;
}

.project-link:hover {
  color: #5eead4;
}

@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.5s ease-out forwards;
}

@keyframes fadeInBot {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .item-card {
    min-height: 350px;
  }
  
  .project-image {
    height: 180px;
  }
}
</style>
