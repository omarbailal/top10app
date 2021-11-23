<template>
    <div class="">
        <nav class="fixed w-full bg-gray-900 md:flex md:items-center ">
            <div class="flex items-center justify-between px-4 py-2">
                <div class="md:hidden">
                    <button @click="isopen = !isopen" class="text-gray-300  focus:outline-none">
                        <svg class="h-8 w-8 fill-current" viewBox="0 0 24 24" >
                            <path v-if="isopen" fill-rule="evenodd" d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"/>
                            <path v-if="!isopen" fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"/>
                        </svg> 
                    </button>
                </div>
                <div class="md:ml-8">
                    <a href="" class="text-indigo-400  font-extrabold text-2xl">TOP <span class="text-gray-400 text-xl -ml-1">10's</span></a>
                </div>
                <div class="md:hidden">
                    <accountDropdown class=""/>
                </div>
            </div>


            <div :class="isopen ? 'block' : 'hidden'" class="text-white  pb-2 md:flex md:ml-4">
                <div class="block py-1 mt-2 ml-3  px-2 md:ml-4 rounded-l md:rounded hover:bg-gray-800 font-semibold">
                    <i class="fas fa-film"></i>
                    <a class="ml-1" href="#">Movies </a>
                </div>
                <div class="block py-1 mt-2 ml-3  px-2 md:ml-4 rounded-l md:rounded hover:bg-gray-800 font-semibold">
                    <i class="fas fa-tv"></i>
                    <a class="ml-1" href="#">Tv shows</a>
                </div>
                <div class="block py-1 mt-2 ml-3  px-2 md:ml-4 rounded-l md:rounded hover:bg-gray-800 font-semibold">
                    <i class="fas fa-user-ninja"></i>
                    <a class="ml-1" href="#">Anime</a>
                </div>
            </div>

            <div class="hidden md:block md:ml-auto md:mr-6">
                <accountDropdown class=""/>
            </div>
        </nav>
    </div>
</template>

<script>
    import accountDropdown from './AccountDropdown';
    export default {
        components: { 
            accountDropdown,
        },
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
