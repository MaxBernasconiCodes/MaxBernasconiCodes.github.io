<template>
  <section class="p-4 bg-white shadow rounded-md">
    <h2 class="text-xl font-semibold mb-2">Skills</h2>
    <ul class="grid grid-cols-2 gap-2">
      <li v-for="skill in skills" :key="skill" class="bg-gray-200 p-2 rounded">
        {{ skill }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        'PHP 7 to 8.2', 'SQL', 'Laravel Framework', 'Eloquent ORM',
        'Blade', 'Livewire', 'TailwindCSS', 'HTML and CSS', 'React',
        'NodeJS', 'ExpressJS', 'JavaScript',
      ],
    };
  },
};
</script>
