<template>
  <nav class="bg-black fixed top-0 left-0 w-full">
    <div class="flex items-center px-4 max-w-7xl mx-auto">
      <div>
        <img class="h-14" src="../assets/logo1.png" />
      </div>
      <div class="ml-auto gap-4 flex">
        <router-link
          class="uppercase font-semibold text-xs text-white cursor-pointer hover:text-gray-600 transition-all"
          v-for="menu in navmenu"
          :key="menu.label"
          :to="menu.to">
          {{ menu.label }}
        </router-link>
      </div>
    </div>
  </nav>
</template>

<script setup>
  const navmenu = [
    { to: '/', label: 'Home' },
    {
      to: '/about',
      label: 'about us',
      submenu: [
        { to: '/our-company', label: 'our company' },
        { to: '/our-team', label: 'our team' },
        { to: '/join-us', label: 'join us' },
      ],
    },
    {
      to: '/about',
      label: 'services',
      submenu: [
        { to: '/account-payroll', label: 'account & payroll' },
        { to: '/admin-support', label: 'admin support' },
        {
          to: '/talent-research-and-lead-generation',
          label: 'talent research and lead generation',
        },
        {
          to: '/it-support',
          label: 'it suppport',
        },
      ],
    },
    { to: '/blog', label: 'blog' },
    { to: '/contact-us', label: 'contact us' },
  ];
</script>
