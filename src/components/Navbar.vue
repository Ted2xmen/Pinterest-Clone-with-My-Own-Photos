<template>
    <div class="px-5 py-2 flex items-center justify-between bg-gradient-to-b from-gray-700 via-gray-900 to-black" >
        <div class="flex items-center gap-3">
            <button class="rounded-full hover:bg-gray-500 flex  items-center justify-center " type="button" name="button">
                <img class="object-contain h-20 w-20" src="https://cdn1.iconfinder.com/data/icons/kind-of-cameras-glyphs/512/14-512.png" alt="logo">
            </button>
            <button  :class="`${selectedTab===item.key ? 'bg-black text-white' : 'text-dark hover:bg-light' } rounded-full py-2 px-5 font-semibold`" v-for="item in tabItems" :key="item.key" @click="selectedTab = item.key">
           <router-link :to="item.path">{{item.name}}</router-link> 
            </button>
        </div>
        <div class="flex-grow relative pl-5">
            <span class="material-icons absolute mt-3 ml-3 text-muted">search</span>
            <input type="text" class="rounded-full py-3 pr-3 pl-10 w-full hover:bg-gray-300  text-muted" placeholder="Search" name="" value="">
        </div>
        <div class="flex items-center gap-1 ">
            <button type="button" name="" class="relative rounded-full hover:bg-gray-100 flex items-center justify-center p-3">
                <span class="material-icons text-3xl">notifications</span>
                <div class="rounded-full h-5 w-5 bg-red-500 text-white flex items-center justify-center mb-5 ml-4 absolute">4</div>
            </button>

              <button type="button" name="" class="relative rounded-full hover:bg-gray-100 flex items-center justify-center p-3">
                <span class="material-icons text-3xl">textsms</span>
                <div class="rounded-full h-5 w-5 bg-red-500 text-white flex items-center justify-center mb-5 ml-4 absolute">1</div>
            </button>
             <button class="rounded-full hover:bg-gray-500 flex  items-center justify-center " type="button" name="button">
                <img class="h-9 w-9 rounded-full object-contain" src="https://pbs.twimg.com/profile_images/1321170490048786436/0EtFIqGA_400x400.jpg" alt="logo">
            </button>
             <button class="rounded-full hover:bg-gray-500 flex  items-center justify-center " type="button" name="button">
                 <span class="material-icons ml-1 ">expand_more</span>
            </button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            tabItems : [
                {name:'Home', key:'home' , path:'/' },
                {name:'About', key:'about' , path: 'about' },
            ],
            selectedTab: 'home'
        }
    },

}
</script>