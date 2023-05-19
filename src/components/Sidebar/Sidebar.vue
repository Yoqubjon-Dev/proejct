<script setup>
    import { DashboardLinks } from '../../constants/DashboardLinks';
</script>

<template>
    <div class="sidebar w-[299px] shadow-lg min-h-screen relative bg-indigo-600">
        <div class="flex pt-10 justify-center items-center">
        <h1 class="px-2 py-1 text-white rounded-xl text-center inline-block w-[48px] h-[48px] text-3xl font-bold bg-red-500">A</h1>
            <a href="/" class="logo inline-block text-center ml-4 text-white text-4xl font-bold">Academy</a>
        </div>

        <div class="list mt-10">
            <a href="/" id="links" class="ml-14 rounded-l-full list__item p-4 block my-2 text-white hover:bg-white hover:text-black duration-100">
              <i class="bx bx-home ml-5"></i> <span class="ms-3">Dashboard</span>
            </a>
            <router-link
              class=" ml-14 rounded-l-full font-bold p-4 block my-2 text-white hover:bg-white hover:text-black duration-100"
              v-for="el in DashboardLinks" :key="el.id"
              :to="el.link"
            >

              <i :class="el.icon" class="ml-5"></i> <span class="ms-3">{{ el.title }}</span>
            </router-link>
          </div>
            <div class="mt-20 ml-20 rounded-l-full font-bold p-4 block my-2 text-white hover:bg-white hover:text-black duration-100">
                <a href="/" class="m-auto font-bold">Chiqish><i class='bx bx-log-out ms-20'></i></a></div>
    </div>
</template>

<style scoped>

    .router-link-active {
        background-color: rgb(253, 250, 252);
        color: black;
    }
</style>