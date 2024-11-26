<template>
  <section class="p-4 bg-white shadow rounded-md">
    <h2 class="text-xl font-semibold mb-2">Education</h2>
    <div class="mb-4">
      <h3 class="text-lg font-medium">{{ education.degree }}</h3>
      <p class="text-sm text-gray-600">{{ education.institution }}</p>
      <p class="text-sm text-gray-600">{{ education.location }}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      education: {
        degree: 'Tecnico Superior en Programacion',
        institution: 'UTN Facultad Regional de Tucuman',
        location: 'Argentina',
      },
    };
  },
};
</script>
