<template>
  <div class="bg-color q-pt-md">
    <div
      class="followers-bg q-mx-sm q-mb-md"
      v-if="$q.screen.lt.md"
      :class="$q.screen.gt.sm ? 'q-px-lg' : 'q-px-sm'"
    >
      <div class="row justify-between flex-center item-center">
        <div>
          <div>Followers</div>
          <div class="q-pt-xs text-h6">1000</div>
        </div>
        <q-separator vertical inset color="white" />
        <div>
          <div>Following</div>
          <div class="q-pt-xs text-h6">500</div>
        </div>
        <q-separator vertical inset color="white" />
        <div>
          <div>Points</div>
          <div class="q-pt-xs text-h6">500</div>
        </div>
      </div>
    </div>
    <div
      class="row justify-between"
      :class="$q.screen.gt.sm ? 'q-px-lg' : 'q-px-md'"
      v-if="$q.screen.lt.md"
    >
      <div class="text-h6">Category</div>
      <div class="text-purple-9 cursor-pointer">View All</div>
    </div>
    <horizontal-list v-if="$q.screen.lt.md" />
    <div
      class="q-mt-xl row justify-center"
      :class="$q.screen.gt.sm ? 'q-px-md' : 'q-mx-sm'"
    >
      <q-item-section top v-if="$q.screen.gt.sm" class="col-3"
        ><box-element :items="itemList" :title="'Category'" />
        <box-element :items="followers" :title="'Following'" class="q-mt-xl"
          ><div class="text-caption">5 Quiz | 200 Points</div></box-element
        >
      </q-item-section>
      <q-item-section
        :class="$q.screen.gt.sm ? 'col-5 q-px-xl' : 'col-12 q-px-xs'"
      >
        <QuizPost :showView="true" />
      </q-item-section>
      <q-item-section top v-if="$q.screen.gt.sm" class="col-3">
        <box-element :items="itemList2" :title="'Category'" />
        <box-element :items="followers" :title="'Top Scores'" class="q-mt-xl" />
      </q-item-section>
    </div>
  </div>
</template>

<script>
import HorizontalList from "../molecules/QuestionHorizontal.vue";
import QuizPost from "../molecules/QuizPost.vue";
import BoxElement from "../molecules/BoxElement.vue";
export default {
  components: {
    QuizPost,
    BoxElement,
    HorizontalList,
  },
  data: () => ({
    itemList: [
      {
        active: true,
        avatar: "science.png",
        title: "Science",
      },
      {
        active: true,
        avatar: "gadgets.png",
        title: "Gadgets",
      },
      {
        avatar: "movie.png",
        title: "Movies",
      },
      {
        avatar: "joystick.png",
        title: "Gaming",
      },
    ],
    itemList2: [
      {
        active: true,
        avatar: "image 4.png",
        title: "Back to School",
      },
      {
        active: true,
        avatar: "image 3.png",
        title: "Do you Know?",
      },
      {
        avatar: "image 5.png",
        title: "World Capital Cities",
      },
      {
        avatar: "image 4.png",
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
