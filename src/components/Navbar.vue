<template>
    <div class="  bg-rose-500 sticky">
        <div class=" text-gray-100 mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8 shadow-black font-bold">

            <!-- mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8 -->
            <div class="flex items-center">
                <RouterLink class="text-2xl" to="/">Lights</RouterLink>
            </div>
        
            <span @click="openMenu()" class="text-gray-100 absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl">
                <i :class="[open ? 'bi bi-x' : 'bi bi-list']"></i>
            </span>
            <ul class="text-gray-100 bg-rose-500 md:flex md:items-center md:px-0 px-6 md:pb-0 pb-10 md:static absolute md:w-auto w-full top-14 duration-300 ease-in" :class="[open ? 'left-0' : 'left-[-100%]']">
                <li class="md:mx-4 md:my-0 my-6">
                    <RouterLink class="text-md hover:text-black" to="/">Home</RouterLink>
                </li>
                <li class="md:mx-4 md:my-0 my-6">
                    <RouterLink class="text-md hover:text-black" to="/menu">Menu</RouterLink>
                </li>
                <li class="md:mx-4 md:my-0 my-6">
                    <!-- <a :href="link.link" class="text-md hover:text-black">{{link.name}}</a> -->
                    <RouterLink class="text-md hover:text-black" to="/about">About Us</RouterLink>
                </li>
                <RouterLink class="bg-black hover:bg-white hover:text-black duration-300 font-xs text-white rounded py-1.5 px-4" to="/contact">Contact Us</RouterLink>
            </ul>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue';


export default {

    setup() {
        const open = ref(false)
        const Links = [
            {name : "Home" , link : "#"},
            {name : "About Us" , link : "#"},
            {name : "Menu" , link : "#"},
        ]

        function openMenu() {
            open.value = !open.value
        }

        return {Links,open,openMenu}
    }
}
</script>