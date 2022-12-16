<template>
    <div class="app-main-layout">
      
      <NavbarVue @IsOpenClik="isOpen = !isOpen"></NavbarVue>
      <SidebarVue :value="isOpen"></SidebarVue>
  
      <main class="app-content" :class="{full:!isOpen}">
        <div class="app-page">
          <router-view />
        </div>
      </main>
  
      <div class="fixed-action-btn">
        <router-link class="btn-floating btn-large" to="/record">
          <i class="large material-icons">add</i>
        </router-link>
      </div>
    </div>
</template>  

<script>
import NavbarVue from '@/components/app/Navbar.vue'
import SidebarVue from '@/components/app/Sidebar.vue'
export default {
    name: 'main-layout',

    data: () => ({
        isOpen:true
    }),

    components:{
        NavbarVue,
        SidebarVue
    },
}
</script>
