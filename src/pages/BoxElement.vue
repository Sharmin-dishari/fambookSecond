<template>
  <div> <q-card flat
      class="border-card">
      <div class="row justify-between q-px-lg q-pt-md">
        <div class="text-h5 text-bold q-mt-md">{{ title }}</div>
        <div class="text-purple-9 cursor-pointer q-pt-md">View All</div>
      </div>
      <q-list class="bordered"
        :class="$q.screen.gt.md ? 'q-px-lg' : 'q-px-sm'">
        <q-item v-for="{ avatar, title, id } in items"
          :key="id"
          v-ripple
          class="q-py-md q-my-lg boxStyle cursor-pointer">
          <q-item-section avatar>
            <q-item-label>
              <q-avatar size="50px"
                lass="q-mt-sm">
                <img :src="avatar" /> </q-avatar></q-item-label>
          </q-item-section>
          <q-item-section class="q-pl-sm text-h6">
            <q-item-label>{{ title }}</q-item-label>
            <q-item-label class="text-caption">@benny_spanbauer</q-item-label>
            <q-item-label>
              <slot />
            </q-item-label>
          </q-item-section>
          <q-item-section side>
            <q-item-label>
              <q-badge label="Following"
                class="web-button q-pa-xs q-px-md"
                rounded />
            </q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
    <q-card flat
      class="
                border-card
                q-mt-lg">
      <div style="margin-top: -50px; margin-left: -80px;"><img src="tips.png" />
      </div>
      <q-card-section class="hintText">
        Offensive power-ups like “2x” give you extra bonus score for
        the right
        answer
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
export default {
  props: {
    items: { type: Array, required: false },
    title: { type: String, default: "Title" },
    description: { type: String, default: "Description" },
  },
};
</script>

<style scoped>
.boxStyle {
  border: 1px solid silver;
  border-radius: 5px;
}

.border-card {
  border: 1px solid silver;
  border-radius: 5px;
}

.hintText {
  font-size: 17px;
  font-weight: 500;
  line-height: 26px;
  letter-spacing: 0em;
  color: #42307D;
  text-align: left;
  margin-top: -30px;
}

.web-button {
  background: #42307D;
}
</style>
