<template>
  <div class="bg-color q-pt-md">
    <div class="row justify-between"
      :class="$q.screen.gt.sm ? 'q-px-lg' : 'q-px-md'"
      v-if="$q.screen.lt.md">
      <div class="text-h6">Category</div>
      <div class="text-purple-9 cursor-pointer">View All</div>
    </div>
    <horizontal-list v-if="$q.screen.lt.md" />
    <q-item-section
      :class="$q.screen.gt.sm ? 'col-5 q-px-xl' : 'col-12 q-px-xs'">
      <QuizPost :showView="true" />
    </q-item-section>
  </div>

</template>

<script>
import HorizontalList from "./QuestionHorizontal.vue";
import QuizPost from "./QuizPost.vue";
import BoxElement from "./BoxElement.vue";
export default {
  components: {
    QuizPost,
    HorizontalList,
  },
  data: () => ({
    itemList: [
      {
        active: true,
        avatar: "Group.png",
        title: "Science",
      },
      {
        active: true,
        avatar: "Group1.png",
        title: "Gadgets",
      },
      {
        avatar: "Group2.png",
        title: "Movies",
      },
      {
        avatar: "Group.png",
        title: "Gaming",
      },
    ],
    itemList2: [
      {
        active: true,
        avatar: "Group.png",
        title: "Back to School",
      },
      {
        active: true,
        avatar: "Group1.png",
        title: "Do you Know?",
      },
      {
        avatar: "Group2.png",
        title: "World Capital Cities",
      },
      {
        avatar: "Group.png",
        title: "Back to School",
      },
    ],
    followers: [
      {
        active: true,
        avatar: "Man.png",
        title: "Riya",
      },
      {
        active: true,
        avatar: "Woman.png",
        title: "Vicky",
      },
      {
        avatar: "Man.png",
        title: "Sharmin",
      },
      {
        avatar: "Woman.png",
        title: "Riya",
      },
    ],
  }),
};
</script>

<style scoped>
.followers-bg {
  border-radius: 20px;
  background: #f04438;
  color: white;
  font-weight: bold;
  text-align: center;
  margin-top: 20px;
  padding: 10px 20px;
}
</style>
