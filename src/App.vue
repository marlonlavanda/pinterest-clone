<template>
  <TopNav></TopNav>
  <div class="px-20 w-full flex flex-wrap">
    <div v-for="(arr, index) in subArrays" :key="index" class="w-1/5 ">
      <div v-for="(card, i) in arr" :key="i" class="w-1full">
        <div class="w-full p-2">
          <Card
            :src="`${card.src}`"
            :board="`${card.recomended}`"
            class="w-full h-full"
          ></Card>
          <div class="text-smal leading-tight pt-2">
            <p class="font-bold">{{ card.title }}</p>
            <p>{{ card.user }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopNav from "./components/TopNav.vue";
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    TopNav,
    Card,
  },
  data() {
    return {
      cards: [
        {
          src: "1.jpg",
          title: "Title 1",
          user: "User 1",
          recomended: "Travel",
        },
        {
          src: "2.jpg",
          title: "Title 2",
          user: "User 2",
          recomended: "Travel",
        },
        {
          src: "3.jpg",
          title: "Title 3",
          user: "User 3",
          recomended: "Travel",
        },
        {
          src: "5.jpg",
          title: "Title 5",
          user: "User 5",
          recomended: "Travel",
        },
        {
          src: "6.jpg",
          title: "Title 6",
          user: "User 6",
          recomended: "Travel",
        },
        {
          src: "7.jpg",
          title: "Title 7",
          user: "User 7",
          recomended: "Travel",
        },
        {
          src: "8.jpg",
          title: "Title 8",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "9.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "4.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "10.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "11.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "12.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "13.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "14.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "15.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "16.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "17.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "18.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "19.jpg",
          title: "Title 4",
          user: "User 4",
          recomended: "Travel",
        },
        {
          src: "20.jpg",
          title: "Title 20",
          user: "User 20",
          recomended: "Travel",
        },
        {
          src: "21.jpg",
          title: "Title 21",
          user: "User 21",
          recomended: "Travel",
        },
        {
          src: "22.jpg",
          title: "Title 22",
          user: "User 22",
          recomended: "Travel",
        },
        {
          src: "23.jpg",
          title: "Title 23",
          user: "User 23",
          recomended: "Travel",
        },
      ],
    };
  },
  computed: {
    subArrays() {
      let length = Math.ceil(this.cards.length / 5);

      const result = new Array(length).fill().map((i) => {
        console.log(i);
        return this.cards.splice(0, length);
      });

      return result;
    },
  },
};
</script>

<style src="./assets/tailwind.css" />
