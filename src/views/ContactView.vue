<script>
export default {
  data() {
    return {
      tech: [
        {
          id: 1,
          name: 'LinkedIN',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/174/174857.png',
          status: 'work',
          url: 'https://www.linkedin.com/in/febryan-riyadi-2705n412'
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://img.icons8.com/m_sharp/200/FFFFFF/github.png',
          status: 'project list',
          url: 'https://github.com/Brazer27'
        },
        {
          id: 3,
          name: 'E-mail',
          imageUrl: 'https://mailmeteor.com/logos/assets/PNG/Gmail_Logo_512px.png',
          status: 'contact me',
          url: 'mailto:febryanriyadi03@gmail.com'
        },
        {
          id: 4,
          name: 'Instagram',
          imageUrl: 'https://cdn-icons-png.freepik.com/256/15789/15789364.png?semt=ais_hybrid',
          status: 'social media',
          url: 'https://www.instagram.com/febryan_4123?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw=='
        }
      ],
      contactInfo: {
        phone: '+62 822 1543 6168',
        email: 'febryanriyadi03@gmail.com',
        location: 'Bandung, West Java, Indonesia'
      }
    };
  },
  methods: {
    openLink(url) {
      window.open(url, '_blank');
    },
    copyToClipboard(text) {
      navigator.clipboard.writeText(text).then(() => {
        // You could add a toast notification here
        console.log('Copied to clipboard:', text);
      });
    }
  }
}
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-teal-50 mx-3">
    <article data-page="contact">
      <header>
        <div class="text-2xl font-bold text-white mb-12 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Get In Touch</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-teal-300">
            Let's connect and discuss opportunities
          </h4>
        </div>
      </header>
      
      <section class="max-w-4xl mx-auto">
        <!-- Contact Information Card -->
        <div class="bg-[#1e1e1f] border border-[#383838] rounded-xl p-8 mb-8 fade-zoom-in">
          <h3 class="text-xl font-bold text-white mb-6 flex items-center gap-3">
            <svg class="w-6 h-6 text-teal-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
            </svg>
            Contact Information
          </h3>
          
          <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <!-- Phone -->
            <div class="contact-info-item group cursor-pointer" @click="copyToClipboard(contactInfo.phone)">
              <div class="flex items-center gap-3 p-4 rounded-lg bg-[#383838] bg-opacity-50 hover:bg-opacity-70 transition-all duration-300 h-20">
                <div class="flex-shrink-0">
                  <svg class="w-5 h-5 text-teal-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                  </svg>
                </div>
                <div class="min-w-0 flex-1">
                  <div class="text-xs text-teal-200 font-medium">Phone</div>
                  <div class="text-white font-medium truncate">{{ contactInfo.phone }}</div>
                </div>
              </div>
            </div>

            <!-- Email -->
            <div class="contact-info-item group cursor-pointer" @click="copyToClipboard(contactInfo.email)">
              <div class="flex items-center gap-3 p-4 rounded-lg bg-[#383838] bg-opacity-50 hover:bg-opacity-70 transition-all duration-300 h-20">
                <div class="flex-shrink-0">
                  <svg class="w-5 h-5 text-teal-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                  </svg>
                </div>
                <div class="min-w-0 flex-1">
                  <div class="text-xs text-teal-200 font-medium">Email</div>
                  <div class="text-white font-medium text-sm truncate">{{ contactInfo.email }}</div>
                </div>
              </div>
            </div>

            <!-- Location -->
            <div class="contact-info-item">
              <div class="flex items-center gap-3 p-4 rounded-lg bg-[#383838] bg-opacity-50 h-20">
                <div class="flex-shrink-0">
                  <svg class="w-5 h-5 text-teal-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                  </svg>
                </div>
                <div class="min-w-0 flex-1">
                  <div class="text-xs text-teal-200 font-medium">Location</div>
                  <div class="text-white font-medium text-sm truncate">{{ contactInfo.location }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Social Media Links -->
        <div class="bg-[#1e1e1f] border border-[#383838] rounded-xl p-8 mb-8 fade-zoom-in">
          <h3 class="text-xl font-bold text-white mb-6 flex items-center gap-3">
            <svg class="w-6 h-6 text-teal-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"></path>
            </svg>
            Connect With Me
          </h3>
          
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
            <div v-for="item in tech" :key="item.id">
              <div @click="openLink(item.url)" class="item-tech flex cursor-pointer items-center gap-4 rounded-lg border border-[#383838] bg-[#1e1e1f] hover:bg-[#282828] hover:border-teal-200 hover:border-opacity-50 p-4 transition-all duration-300 hover:transform hover:-translate-y-1 h-20">
                <div class="flex h-12 w-12 items-center justify-center rounded-lg bg-[#383838] bg-opacity-50 zoom-in flex-shrink-0">
                  <img :src="item.imageUrl" alt="Contact Logo" loading="lazy" class="img-tech drop-shadow-xl transition-all duration-300 h-8 w-8 object-contain" />
                </div>
                <div class="flex-1 min-w-0">
                  <div class="tech font-medium text-white transition-all duration-300 truncate">{{ item.name }}</div>
                  <div class="text-xs text-teal-200 opacity-75 transition-all duration-300 truncate">
                    {{ item.status }}
                  </div>
                </div>
                <div class="flex-shrink-0">
                  <svg class="w-4 h-4 text-teal-200 opacity-50 group-hover:opacity-100 transition-all duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path>
                  </svg>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Call to Action -->
        <div class="bg-[#1e1e1f] border border-[#383838] rounded-xl p-8 text-center fade-zoom-in">
          <h3 class="text-xl font-bold text-white mb-4">Ready to Start a Conversation?</h3>
          <p class="text-[#a1a1aa] mb-6 max-w-2xl mx-auto">
            I'm always open to discussing new opportunities, interesting projects, or just having a friendly chat about technology and development.
          </p>
        </div>
      </section>
    </article>
  </div>
</template>

<style scoped>
/* Consistent hover effects */
.item-tech:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
}

.item-tech:hover .img-tech {
  transform: scale(1.1);
}

.contact-info-item:hover {
  transform: translateY(-2px);
}

/* Animations */
@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.95);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

.fade-zoom-in {
  animation: fadeZoomIn 0.8s ease-out;
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.6s ease-out forwards;
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

.zoom-in {
  transition: transform 0.3s ease;
}

/* Responsive improvements */
@media (max-width: 640px) {
  .item-tech {
    flex-direction: column;
    text-align: center;
    gap: 2;
  }
  
  .item-tech .flex-1 {
    margin-top: 0.5rem;
  }
}

/* Enhanced gradient text for subtitle */
.title-section h4:last-child {
  background: linear-gradient(135deg, #f1f5f9 0%, #5eead4 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
</style>
