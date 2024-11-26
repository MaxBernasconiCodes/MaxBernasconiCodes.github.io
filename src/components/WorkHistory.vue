<template>
  <section class="p-4 bg-white shadow rounded-md">
    <h2 class="text-xl font-semibold mb-2">Work History</h2>
    <div v-for="job in workHistory" :key="job.title" class="mb-4">
      <h3 class="text-lg font-medium">{{ job.title }} - {{ job.company }}</h3>
      <p class="text-sm text-gray-600">{{ job.dates }}</p>
      <ul class="list-disc ml-5">
        <li v-for="duty in job.duties" :key="duty">{{ duty }}</li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      workHistory: [
        {
          title: 'Full Stack Web Developer',
          company: 'Autonomous',
          dates: '03.2018 - Current',
          duties: [
            'Used PHP, SQL, HTML, and CSS to develop app solutions.',
            'Reviewed code, debugged problems, and corrected issues.',
            'Analyzed existing software implementations.',
          ],
        },
        {
          title: 'Backend Developer',
          company: 'Telecom Argentina',
          dates: '04.2022 - 03.2023',
          duties: [
            'Built APIs and data clients to consume APIs.',
            'Managed efficient SQL queries.',
            'Worked in Agile Scrum teams.',
          ],
        },
      ],
    };
  },
};
</script>
