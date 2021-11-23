<template>
    <div class="relative">
        <div class="flex">
            <button @click="isopen = !isopen" class="flex items-center px-2 py-1 hover:bg-gray-800  rounded-full overflow-hidden focus:outline-none">
                <img class="block rounded-full h-8 w-8 object-cover" src="https://www.venmond.com/demo/vendroid/img/avatar/big.jpg" alt="">
                <span class="hidden md:block text-sm text-white font-semibold ml-2 ">Name</span>
                <i class="fas fa-chevron-down fa-sm text-white ml-1 mt-1"></i>
            </button>
        </div>
        <div :class="isopen ? 'block' : 'hidden'" class="w-32 mt-2 py-2 absolute right-0 bg-white rounded-lg text-gray-700 font-semibold border"> 
            <div class="flex items-center px-4 py-2 hover:text-black ">
                <i class="fas fa-user-alt"></i>
                <a class="ml-2" href="#">Profile</a>
            </div>
            <div class="flex items-center px-4 py-2 hover:text-black ">
                <i class="fas fa-user-cog"></i>
                <a class="ml-2" href="#">Settings</a>
            </div>
            <div class="flex items-center px-4 py-2 hover:text-black ">
                <i class="fas fa-sign-out-alt"></i>
                <a class="ml-2" href="#">Sign out</a>
            </div>
            
        </div> 
    </div>
</template>

<script>
    export default {
        data(){
            return {
                isopen: false,
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
