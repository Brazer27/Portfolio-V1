<script>
export default {
  data() {
    return {
      activeTab: 1,
      certificates: [
        {
          id: 1,
          title: 'Fundamental Data Science',
          issuer: 'Coding Studio',
          issuedDate: 'December 2024',
          imageUrl: 'fundamentalds',
          description: 'A comprehensive introduction to essential data science tools and techniques using Python, focusing on data manipulation, analysis, and visualization.',
          skills: ['Data Visualization', 'Data Preprocessing', 'Python Scripting & Shell Commands', 'Exploratory Data Analysis (EDA)'],
          credentialId: 'McN0Cn1Wax',
          verificationUrl: 'https://member.codingstudio.id/certificate/McN0Cn1Wax'
        },
        {
          id: 2,
          title: 'Intermediate Data Science',
          issuer: 'Coding Studio',
          issuedDate: 'December 2024',
          imageUrl: 'intermediateds',
          description: 'A program focused on developing machine learning skills using Python and Scikit-Learn, including data preparation, linear and polynomial regression, pipeline creation, and model validation techniques.',
          skills: ['Model Evaluation & Metrics', 'Regression Analysis', 'Supervised Machine Learning', 'Scikit-Learn Framework'],
          credentialId: 'r3Qdj8B8AP',
          verificationUrl: 'https://member.codingstudio.id/certificate/r3Qdj8B8AP'
        },
        {
          id: 3,
          title: 'Professional Application Database Development with SQL Server',
          issuer: 'Coding Studio',
          issuedDate: 'June 2025',
          imageUrl: 'database',
          description: 'A hands-on course on professional database development using SQL Server, covering SQL fundamentals, advanced querying, database design, and security management.',
          skills: ['SQL', 'Relational Database Design', 'Microsoft SQL Server', 'Data Manipulation & Query Optimization'],
          credentialId: 'sHmTK9Re54',
          verificationUrl: 'https://member.codingstudio.id/certificate/sHmTK9Re54'
        },
        {
          id: 4,
          title: 'Mastering Modern Website Development with React JS',
          issuer: 'Coding Studio',
          issuedDate: 'June 2025',
          imageUrl: 'react',
          description: 'A comprehensive certification that equips learners with foundational to advanced skills in React.js, enabling them to build and deploy dynamic, modern web applications.',
          skills: ['React Hooks', 'Frontend Styling', 'JavaScript ES6+', 'React.js Development', 'UI Integration'],
          credentialId: 'RH5UtUaRYb',
          verificationUrl: 'https://member.codingstudio.id/certificate/RH5UtUaRYb'
        },
        {
          id: 5,
          title: 'HIPAA Compliance',
          issuer: 'Udemy',
          issuedDate: 'July 2025',
          imageUrl: 'hipaa',
          description: 'This certification provides foundational knowledge of HIPAA regulations, privacy and security rules, and how to handle protected health information (PHI) responsibly and compliantly.',
          skills: ['HIPAA Compliance', 'Data Privacy and Security', 'Healthcare Information Security', 'Protected Health Information (PHI) Management'],
          credentialId: 'UC-8b910fc1-6a81-4b5c-8a02-3ef8dd2f91f2',
          verificationUrl: 'https://www.udemy.com/certificate/UC-8b910fc1-6a81-4b5c-8a02-3ef8dd2f91f2/'
        }
      ],
    };
  },
  computed: {
    sortedCertificates() {
      return [...this.certificates].sort((a, b) => {
        return new Date(b.issuedDate) - new Date(a.issuedDate);
      });
    }
  }
}
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-teal-50 mx-3">
    <article data-page="certificates">
      <header>
        <div class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Certifications & Learning</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-teal-300">
            Professional development and continuous learning journey
          </h4>
        </div>
      </header>
      
      <section>
        <!-- My Certificates Tab -->
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-1 gap-6 pb-32 md:grid-cols-2 lg:grid-cols-2 xl:gap-8 fade-zoom-in">
            <div v-for="cert in sortedCertificates" :key="cert.id">
              <div class="cert-card flex flex-col gap-4 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-teal-50 p-6 h-full transition-all duration-300">
                <!-- Certificate Image -->
                <div class="cert-image-container">
                  <img alt="Certificate Image" 
                       loading="lazy" 
                       decoding="async" 
                       class="cert-image drop-shadow-xl rounded-xl w-full object-cover"
                       :src="'/img/certificate-' + cert.imageUrl + '.png'">
                </div>
                
                <!-- Certificate Content -->
                <div class="flex flex-col gap-3 flex-grow">
                  <div class="cert-header">
                    <div class="cert-title font-bold text-lg text-white mb-1">
                      {{ cert.title }}
                    </div>
                    <div class="cert-issuer text-teal-200 font-medium text-sm mb-2">
                      {{ cert.issuer }}
                    </div>
                    <div class="cert-date text-xs text-[#c1c1c1] bg-[#383838] px-2 py-1 rounded-full inline-block">
                      Issued: {{ cert.issuedDate }}
                    </div>
                  </div>
                  
                  <div class="cert-description text-sm text-[#c1c1c1] leading-relaxed flex-grow">
                    {{ cert.description }}
                  </div>
                  
                  <!-- Skills Tags -->
                  <div class="cert-skills mb-4">
                    <div class="flex flex-wrap gap-2">
                      <span v-for="skill in cert.skills" :key="skill" 
                            class="bg-teal-200 bg-opacity-10 text-teal-200 px-2 py-1 rounded-full text-xs">
                        {{ skill }}
                      </span>
                    </div>
                  </div>
                  
                  <!-- Certificate Links and Info -->
                  <div class="cert-footer">
                    <div class="text-xs text-[#c1c1c1] mb-3">
                      <span class="font-medium">Credential ID:</span> {{ cert.credentialId }}
                    </div>
                    <div class="flex justify-between items-center">
                      <a v-if="cert.verificationUrl"
                         :href="cert.verificationUrl" 
                         target="_blank" 
                         rel="noreferrer"
                         class="cert-verify-btn bg-teal-200 bg-opacity-10 hover:bg-opacity-20 text-teal-200 px-4 py-2 rounded-lg text-sm font-medium transition-all duration-200 hover:scale-105">
                        Verify Certificate
                      </a>
                      
                      <div class="cert-icon">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" 
                             stroke-linecap="round" stroke-linejoin="round" height="24" width="24" 
                             xmlns="http://www.w3.org/2000/svg" class="text-teal-200">
                          <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"></path>
                          <polyline points="22 4 12 14.01 9 11.01"></polyline>
                        </svg>
                      </div>
                    </div>
                  </div>
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
.cert-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  min-height: 500px;
}

.cert-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.cert-image-container {
  width: 100%;
  aspect-ratio: 3/2;
  overflow: hidden;
  border-radius: 0.75rem;
}

.cert-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.cert-card:hover .cert-image {
  transform: scale(1.05);
}

.cert-verify-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

.cert-verify-btn:hover {
  text-decoration: none;
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

/* Timeline connector line */
.space-y-4 > div::before {
  content: '';
  position: absolute;
  left: 1.375rem;
  top: 0.875rem;
  width: 1px;
  height: calc(100% + 1rem);
  background-color: #383838;
  z-index: -1;
}

.space-y-4 > div:last-child::before {
  display: none;
}

.space-y-4 {
  position: relative;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .cert-card {
    min-height: 450px;
  }
  
  .grid-cols-1.md\\:grid-cols-2.lg\\:grid-cols-2 {
    grid-template-columns: 1fr;
  }
}

@media (min-width: 768px) {
  .grid-cols-1.md\\:grid-cols-2.lg\\:grid-cols-2 {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>