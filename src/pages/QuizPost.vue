<template>
  <div class="row justify-center">
    <div avatar
      v-if="$q.screen.gt.sm"
      class="col-3"><box-element :items="itemList"
        :title="'Top Scorers'" />
    </div>
    <div :class="$q.screen.gt.sm ? 'col-4 q-mx-md' : 'col-12 q-px-xs'">
      <q-item-label>
        <q-card class="border-card shadow-8 shadow-15 q-mb-md">
          <q-card-section top
            class="q-pa-none q-px-md q-py-sm">
            <div class="row no-wrap">
              <div class="col">
                <div class="row q-gutter-x-md items-center">
                  <q-item-label>
                    <q-avatar size="45px"
                      lass="q-mt-sm">
                      <img src="Group1.png" /> </q-avatar></q-item-label>
                  <div class="q-mt-xs">
                    <div class="row titleFont">
                      <div>Raheel Khan</div>
                      <div>
                        <q-btn
                          class="q-px-xs web-button text-white q-ml-sm followbtn"
                          size="8px"
                          dense
                          no-caps
                          unelevated
                          label="Following" />
                      </div>
                    </div>
                    <div class="text-subcaption q-mt-xs">25 March 2024, 01:03 pm
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-auto">
                <q-btn color="grey-7"
                  round
                  flat
                  icon="more_vert">
                  <q-menu cover
                    auto-close>
                    <q-list>
                      <q-item clickable>
                        <q-item-section>Remove Card</q-item-section>
                      </q-item>
                      <q-item clickable>
                        <q-item-section>Send Feedback</q-item-section>
                      </q-item>
                      <q-item clickable>
                        <q-item-section>Share</q-item-section>
                      </q-item>
                    </q-list>
                  </q-menu>
                </q-btn>
              </div>
            </div>
          </q-card-section>

          <q-card-section class="q-py-none titleFont">
            Do Your know the basic science questions?
          </q-card-section>
          <q-card-section>
            <!-- <q-parallax src="yellow.png"
                :height="250" /> -->
            <q-img src="yellow.png"
              alt="" />
          </q-card-section>
          <q-separator class="addMargin" />
          <q-item class="row justify-end q-pb-none q-my-none text-color">
            <div class="q-gutter-x-md">
              <q-btn flat
                size="10px"
                label="120"
                :icon="'img:/like.svg'"
                dense>
              </q-btn>
              <q-btn flat
                size="10px"
                label="120"
                :icon="'img:/question.svg'"
                dense>
              </q-btn>
              <q-btn flat
                size="10px"
                label="120"
                :icon="'img:/share.svg'"
                dense>
              </q-btn>
            </div>
          </q-item>
        </q-card>
      </q-item-label>
      <q-item-label>
        <q-card class="border-card q-pt-none shadow-8 shadow-15">
          <div class="q-px-md q-py-md">
            <div class="q-pb-sm titleFont">
              30 Questions to Answer in 30 Minutes
            </div>
            <div>
              <div>
                <q-btn class="full-width text-white q-py-xs web-button"
                  label="START" />
              </div>
              <div>
                <q-btn class="full-width q-mt-md  backBtn"
                  label="Go Back"
                  no-caps
                  outline
                  unelevated />
              </div>
            </div>
          </div>
        </q-card>
      </q-item-label>
    </div>
  </div>
</template>

<script>
import BoxElement from "./BoxElement.vue";
export default {
  components: {
    BoxElement,
  },
  data: () => ({
    itemList: [
      {
        active: true,
        avatar: "Group1.png",
        title: "Kevin",
      },
      {
        active: true,
        avatar: "Group.png",
        title: "Austin",
      },
      {
        avatar: "Group2.png",
        title: "DUstin",
      },
      {
        avatar: "Group.png",
        title: "Jacob",
      },
      {
        active: true,
        avatar: "Group1.png",
        title: "Kevin",
      },
      {
        active: true,
        avatar: "Group.png",
        title: "Austin",
      },
    ],
  }),
};
</script>

<style scoped>
.web-button {
  background: #42307D;
}
</style>
