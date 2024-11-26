<template>
  <div id="resume" class="min-h-screen bg-gray-100 text-gray-800">
    
    <header class="bg-primary text-white p-4 flex justify-between items-center">
      <span>
        <img src="/android-chrome-192x192.png" alt="Maximiliano Bernasconi" class="w-16 h-16 opacity-50">
      </span>
      <span>
        <h1 class="text-center text-3xl font-bold">Maximiliano Bernasconi</h1>
        <p class="text-center">Full Stack Developer</p>
      </span>
      <span>
        <button @click="downloadPDF" class="bg-blue-500 text-white px-4 py-2 rounded">
          Download as PDF
        </button>
      </span>
    </header>
    <main class="p-6 space-y-8 max-w-5xl mx-auto min-w-[800px]">
      <ProfessionalSummary />
      <ContactInfo />
      <Skills />
      <WorkHistory />
      <Education />
      <Languages />
    </main>
    <footer class="bg-secondary text-white text-center p-4">
      © 2024 Maximiliano Bernasconi
    </footer>
  </div>
</template>

<script>
import ProfessionalSummary from './components/ProfessionalSummary.vue';
import ContactInfo from './components/ContactInfo.vue';
import Skills from './components/Skills.vue';
import WorkHistory from './components/WorkHistory.vue';
import Education from './components/Education.vue';
import Languages from './components/Languages.vue';
import html2pdf from 'html2pdf.js';

export default {
  components: {
    ProfessionalSummary,
    ContactInfo,
    Skills,
    WorkHistory,
    Education,
    Languages,
  },
  methods: {
    downloadPDF() {
      const element = document.querySelector('main');
      const date = new Date();
      const month = date.toLocaleString('default', { month: 'short' }); 
      const year = date.getFullYear(); 

      const filename = `CV-Maximiliano Bernasconi-${month.toUpperCase()}-${year}.pdf`;

      const options = {
        margin: 1,
        filename: filename,
        image: { type: 'jpeg', quality: 0.98 },
        html2canvas: { scale: 2 },
        jsPDF: { unit: 'in', format: 'letter', orientation: 'portrait' }
      };

      html2pdf().set(options).from(element).save();
    }
  }
};
</script>
