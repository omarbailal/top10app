<template>
    <div class="align-middle ">
       <div class="flex items-center ">
            <div class="hidden md:block  mx-auto mt-10 whitespace-no-wrap">
                <h1 class="text-indigo-500 font-extrabold text-4xl lg:text-5xl ml-5">This is my TOP<span class="text-2xl lg:text-4xl ml-1">10's</span> </h1>
                <h4 class="text-gray-800 font-bold text-xl lg:text-2xl my-6 ml-5">You didn't like it?</h4>
                <button class="text-base lg:text-lg text-indigo-500 border-2 border-indigo-500 hover:text-white hover:bg-indigo-500 font-bold rounded-md ml-5 py-2  w-10/12">Show me yours</button>
            </div>
            <div class="mx-auto mt-20 sm:w-2/3 md:w-1/2">
                <div class="mx-2 mb-5">
                <h1 class="md:hidden text-center text-indigo-600 font-extrabold text-4xl mb-3 w-full">This is my TOP<span class="text-2xl ml-1">10's</span> </h1>
                <mytop10/>
                <h4 class="md:hidden text-gray-800 text-center font-bold text-2xl my-6">You didn't like it?</h4>
                <div class="text-center">
                    <button  class="md:hidden text-xl text-white bg-indigo-500 hover:bg-indigo-400 font-bold rounded-md py-3  w-10/12">Show me yours</button>
                </div>
                </div>
            </div>  
        </div>
    </div>
</template>

<script>
    import mytop10 from './MyTop10';
    export default {
        components: { 
            mytop10,
        },
        data(){
            return {
               
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
