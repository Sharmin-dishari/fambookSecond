<template>
  <div>
    <q-card class="border-card shadow-8 shadow-15">
      <div class="row justify-between q-px-md">
        <div class="titleFont text-bold q-mt-xs">{{ title }}</div>
        <div
          class="text-color text-caption text-weight-medium cursor-pointer q-pt-sm">
          View All
        </div>
      </div>
      <q-list class="q-px-sm">
        <q-item v-for="{ avatar, title, active, id } in items"
          :key="id"
          v-ripple
          class="cursor-pointer q-pa-none q-py-xs">
          <q-item-section avatar>
            <q-item-label>
              <q-avatar size="42px"
                lass="q-mt-sm">
                <img :src="avatar" /> </q-avatar></q-item-label>
          </q-item-section>
          <q-item-section>
            <q-item-label class="text-caption text-bold">{{ title
              }}</q-item-label>
            <q-item-label
              class="text-grey text-subcaption">@benny_spanbauer</q-item-label>
            <q-item-label>
              <slot />
            </q-item-label>
          </q-item-section>
          <q-item-section side>
            <q-item-label>
              <q-badge label="Follow"
                size="10px"
                v-if="active"
                class="web-button q-pa-xs q-px-sm"
                rounded />
              <q-badge label="Following"
                size="10px"
                v-else
                outline
                class="q-pa-xs q-px-sm text-color bg-white"
                rounded />
            </q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
    <q-card class="q-mt-md shadow-8 shadow-15 border-card">
      <div>
        <img src="tipss.svg"
          class="tips-image" />
      </div>
      <q-card-section class="hintText">
        Offensive power-ups like “2x” give you extra bonus score for the right
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
.border-card {
  border-radius: 5px;
}

.hintText {
  font-size: .9rem;
  font-weight: 500;
  line-height: 26px;
  letter-spacing: 0em;
  color: #42307d;
  text-align: left;
  margin-top: -30px;
}

.web-button {
  background: #42307d;
}

.tips-image {
  margin-top: -30px;
  margin-left: -40px;
  width: 100px;
  height: 90px;
}
</style>
