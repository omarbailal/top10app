<template>
<div class="flex items-center">
    <div class="text:xl md:text-2xl font-semisolid mr-3 lg:mr-6 lg:ml-4">
        {{item.id}}
    </div>
    <div class="flex mr-3 lg:mr-6 ">
        <button @click="up" class="text-green-500 text-sm md:text-base hover:text-green-600 mr-2 lg:mr-4 focus:outline-none">
            <i class="fas fa-arrow-up fa-lg"></i>
            <p class="font-bold">{{item.up}}</p>
        </button>
        <button @click="down" class="text-red-500 text-sm md:text-base  hover:text-red-600 focus:outline-none">
            <i class="fas fa-arrow-down fa-lg"></i>
            <p class="font-bold">{{item.down}}</p>
        </button>
    </div>
    <div class=" mb-2 mr-3 lg:mr-6 border-2 border-gray-400 w-3/12 sm:w-2/12 ">
        <img class="h-16 lg:h-24 w-full object-cover" :src="item.img" alt="">
    </div>
    <div class=" lg:mr-4 -mt-2 w-5/12 ">
        <h1 class="font-bold text-base md:text-xl text-gray-800 ">{{item.title}}</h1>
        <p class=" font-semibold text-xs text-gray-700 ">{{item.desc}}</p>
    </div>
</div>

</template>

<script>
    export default {
        data(){
            return {

            }
        },
        props: ["item"],
        methods: {
            up(){
                this.item.up++;
            },
            down(){
                this.item.down++;
            },

        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
