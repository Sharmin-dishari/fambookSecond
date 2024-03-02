<template>
  <q-page class="bg-color">

    <q-item class="row q-pt-md justify-center q-px-md scroll">
      <q-item-section top
        v-if="$q.screen.gt.sm"
        class="col-3"><box-element :items="itemList"
          :title="'Top Scorers'" />
      </q-item-section>
      <q-item-section top
        :class="$q.screen.gt.sm ? 'col-6 q-pl-xl' : 'col-12 q-px-xs'">
        <q-item-label>
          <div flat
            class="bg-grey-1 border-card">
            <q-card-section top>
              <div class="row no-wrap">
                <div class="col">
                  <div class="row q-gutter-x-md items-center">
                    <q-item-label>
                      <q-avatar size="50px"
                        lass="q-mt-sm">
                        <img src="Group1.png" /> </q-avatar></q-item-label>
                    <div>
                      <div class="row">
                        <div class="text-h6">Rahim Diaz</div>
                        <div class="q-pt-sm">
                          <q-btn
                            class="q-px-xs web-button text-white q-ml-sm followbtn"
                            size="8px"
                            dense
                            label="Following" />
                        </div>
                      </div>
                      <div class="text-caption">25 March 2023, 01:03 pm</div>
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

            <q-card-section class="text-h6 q-pt-none">
              Basic Science question for all age group.
            </q-card-section>
            <q-card-section>
              <q-parallax src="yellow.png"
                :height="250" />
            </q-card-section>

            <!-- <q-separator class="addMargin" /> -->
          </div>
        </q-item-label>
        <q-item-label class="">
          <div flat
            class="bg-grey-1 q-mb-md border-card q-pt-none">
            <div class="q-px-md q-py-md q-mb-md">
              <div class="q-pb-sm text-h6">
                30 Questions to Answer in 30 Minutes
              </div>
              <div>
                <div>
                  <q-btn class="full-width text-white q-py-xs web-button"
                    label="START" />
                </div>
                <div>
                  <q-btn class="full-width q-mt-md text-purple-4 backBtn"
                    label="Back"
                    unelevated />
                </div>
              </div>
            </div>
          </div>
        </q-item-label>
      </q-item-section>
    </q-item>
  </q-page>
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
        title: "Riya",
      },
      {
        active: true,
        avatar: "Group.png",
        title: "Vicky",
      },
      {
        avatar: "Group2.png",
        title: "Sharmin",
      },
      {
        avatar: "Group.png",
        title: "Riya",
      },
    ],
  }),
};
</script>

<style scoped>
.backBtn {
  background: #f9f5ff;
  border: 1px solid #9e77ed;
}

.web-button {
  background: #42307D;
}

.border-card {
  border: 1px solid silver;
  border-radius: 5px;
}

.nextButton {
  background: #9e77ed;
}
</style>
