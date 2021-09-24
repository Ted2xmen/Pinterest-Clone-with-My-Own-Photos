<template>
    <div class="relative" @mouseover="hover = true" @mouseleave="hover = false">

        <img :src="srcImage" alt="" class="rounded-lg">
        <div v-if="hover" class="absolute bg-black opacity-80 inset-0 w-full h-full rounded-lg">
            <div v-if="hover" class="absolute top-0 w-full h-full flex flex-col justify-between">
                <div class="flex items-center justify-between p-3">

                    <button class="flex items-center">
                        <p class="font-semibold text-white">{{board}}</p>
                         <span class="material-icons">expand_more</span>
                    </button>

                    <button class="rounded-full  py-3 px-3 text-white bg-red-900 font-semibold">
                       Save
                    </button>

                </div>

<div class="flex items-center">

    <button class="bg-white rounded-full  w-8 h-8 flex items-center justify-center  py-1 px-1  text-dark opacity-80 hover:opacity-100 m-1">
        <span class="material-icons text-base">ios_share</span>
    </button>
     <button class="bg-white rounded-full w-8 h-8 flex items-center justify-center py-1  px-1  text-dark opacity-80 hover:opacity-100 m-1">
        <span class="material-icons text-base">more_horiz</span> 
    </button>
    <span class="flex items-end justify-center text-white" :user="user" >{{user}}</span>
</div>

            </div>

        </div>
    

    </div>
</template>



<script>
export default {
    name: 'Card',
    props: ['srcImage' , 'board' ,'user'],
    data(){
        return{
            hover:true
        }
    }
}
</script>