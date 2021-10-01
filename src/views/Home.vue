<template>
  <div class="home">
    <div>
      <div class="px-20 py-6 w-full flex flex-wrap">
        <div v-for="(card, index) in cards" :key="index" class="w-1/5">
          <div class="w-full p-2">
            <Card
              :user="`${card.user}`"
              :board="`${card.title}`"
              class="w-full h-full"
              :srcImage="`${card.src}`"
            />
            <div class="text-sm"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "@/components/Card.vue";

export default {
  name: "Home",
  components: {
    Card,
  },

  data() {
    return {
      cards: [
        {
          src: "https://assets.community.lomography.com/75/075b2348818cf352d917d7e2438a524627a194/386x256x2.jpg?auth=adcd759019c8497da4018a84edf53d794f88dc31",
          title: "Ankara",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/28/f838dea1df8e2c6da64b40b78070c3c184bfa4/379x256x2.jpg?auth=23d32ba0c6b0e8518c7202910173be6db3739283",
          title: "Karşıyaka",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/5a/601f2ee8afacb28ab6b963b87d2061c39a9840/379x256x2.jpg?auth=3d1c1cb1e42f794394e93a216cbd5c34628d4959",
          title: "Taksim",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/20/a3b429c092960fb665147a2914a8e9f2cad6b7/1216x821x1.jpg?auth=f22bee94558dee08d8c40d5909045b6e672fb677",
          title: "Me",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/5c/9b4ea9eb296db2a214bad93647bdc5a3748092/1216x821x1.jpg?auth=fe8696f9d11bd7ba12f368d9d33c66903c1b6caf",
          title: "Eminönü",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/9c/3c09d2d4d11efb207441296b7dc2389e3b30f5/1216x806x2.jpg?auth=682e8fefbba8aabe2e0fd2cf64b78e24f224e269",
          title: "Ankara",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/b8/0898ce5415c655aa41d07bec2edec8c9cb87ac/1818x1228x2.jpg?auth=def275d11a5e4aa27d5def581a6f404277bae2fe",
          title: "Kadıköy/Moda",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/1a/952da580e65cbe1b09476e9dbe1ceb26aa2724/1818x1228x2.jpg?auth=1d940b8a19f4172b8406d952659b44790bbba2b9",
          title: "İstanbul",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/6a/db005cc4c43979d5b19a529a8598904ac5fcd8/1216x806x2.jpg?auth=0c4befa4f4ff69e8ec688d29deadca089f408773",
          title: "Kadıköy/Moda",
          user: "Tugrul",
        },
        {
          src: "https://assets.community.lomography.com/be/6f67cce2d88dda6cc9304a0453b662db97d6ea/1216x821x1.jpg?auth=ae8b963e35182425191ae907ac9f10b55f316b5d",
          title: "Kuzguncuk",
          user: "Tugrul",
        },
      ],
    };
  },
};
</script>


