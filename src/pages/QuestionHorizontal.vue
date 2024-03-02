<template>
  <div>
    <div class="horizontal-scroll-container q-mb-sm q-py-xs">
      <div class="item q-mx-sm"
        v-for="item in itemList"
        :key="item.id">
        <q-avatar><img :src="item.avatar"></q-avatar>
        <div>{{ item.title }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itemList: [
        {
          avatar: "Group.png",
          title: "Kevin",
        },
        {
          avatar: "Group2.png",
          title: "Dustin",
        },
        {
          avatar: "Group1.png",
          title: "Rimon",
        },
        {
          avatar: "Group.png",
          title: "Gobinda",
        },
        {
          avatar: "Group1.png",
          title: "Tumpa",
        },
        {
          avatar: "Group2.png",
          title: "Kevin",
        },
        {
          avatar: "Group.png",
          title: "Movies",
        },
        {
          avatar: "Group1.png",
          title: "Kyling",
        },
      ],
    };
  },
};
</script>

<style scoped>
.horizontal-scroll-container {
  overflow-x: auto;
  position: relative;
  white-space: nowrap;
}

.item {
  display: inline-block;
  /* Adjust the width as per your requirements */
  text-align: center;
}
</style>
