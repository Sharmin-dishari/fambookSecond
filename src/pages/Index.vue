<template>
  <q-page padding>
    <div v-if="$q.screen.lt.md"
      class="q-mx-sm">
      <img src="/smatur-logo.svg" />
      <div class="row justify-between q-ma-xs text-bold text-color">
        <div class="text-h6">Top Scorers</div>
        <div class="cursor-pointer">View All</div>
      </div>
      <horizontal-list />
    </div>
    <q-item-section>
      <QuizPost :showView="true" />
    </q-item-section>
  </q-page>

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
