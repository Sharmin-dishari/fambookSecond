<template>
  <div :class="$q.screen.gt.md ? 'q-px-lg' : 'q-px-sm'">
    <div class="horizontal-scroll-container q-mt-md q-mb-sm q-pt-md q-pb-md">
      <div class="item q-px-md"
        v-for="item in itemList"
        :key="item.id">
        <img :src="item.avatar"
          alt="Item Image" />
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
          title: "Back to School",
        },
        {
          avatar: "Group2.png",
          title: "Do you Know?",
        },
        {
          avatar: "Group1.png",
          title: "World Capital Cities",
        },
        {
          avatar: "Group.png",
          title: "Back to School",
        },
        {
          avatar: "Group1.png",
          title: "Science",
        },
        {
          avatar: "Group2.png",
          title: "Gadgets",
        },
        {
          avatar: "Group.png",
          title: "Movies",
        },
        {
          avatar: "Group1.png",
          title: "Gaming",
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
