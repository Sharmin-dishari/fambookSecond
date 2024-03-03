<template>
  <q-layout q-layout view="lHh Lpr lFf">
    <q-header class="bgColor">
      <q-toolbar
        class="row justify-between q-px-lg"
        :class="$q.screen.gt.sm ? 'q-py-xs' : 'q-py-md'"
      >
        <div class="" v-if="$q.screen.gt.sm">
          <div v-if="$route.path !== '/quiz-paper'">
            <img src="/logo.svg" alt="" height="58px" width="160px" />
          </div>
          <div v-else>
            <div class="row items-center">
              <div class="q-py-xs">
                <q-avatar size="50px" lass="q-mt-sm">
                  <img src="Group1.png" />
                </q-avatar>
              </div>
              <div class="q-ml-sm">Raheel Khan</div>
              <div>
                <q-btn
                  class="q-px-xs bg-deep-orange-5 text-white q-ml-sm followbtn"
                  size="10px"
                  dense
                  no-caps
                  unelevated
                  label="Following"
                />
              </div>
            </div>
          </div>
        </div>
        <div
          class="row text-center q-gutter-x-md headerFont text-white"
          v-if="$q.screen.gt.sm"
        >
          <div class="cursor-pointer">HOME</div>
          <div>CATEGORIES</div>
          <div>ABOUT US</div>
        </div>
        <div v-else>
          <q-btn
            flat
            round
            color="white"
            size="14px"
            icon="menu"
            v-if="$q.screen.lt.md"
          >
            <q-menu content-class="bg-purple text-white" auto-close>
              <q-list>
                <q-item clickable to="/home-index">
                  <q-item-section>Home</q-item-section>
                </q-item>
                <q-item clickable>
                  <q-item-section>Categories</q-item-section>
                </q-item>
                <q-separator dark />
                <q-item clickable>
                  <q-item-section>About Us</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-if="$q.screen.lt.md && this.$route.path === '/home-index'"
                  to="/dashboard-index"
                >
                  <q-item-section>Login</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-if="$q.screen.lt.md && this.$route.path !== '/home-index'"
                >
                  <q-item-section>Profile</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </q-btn>
        </div>

        <div>
          <q-btn
            icon="chevron_left"
            color="white"
            @click="$router.back()"
            class="text-black q-py-xs"
            label="GO BACK"
          />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container class="background-image">
      <router-view />
    </q-page-container>
    <q-footer
      class="backdrop-effect text-primary shadow-24 footer"
      v-if="$q.screen.lt.sm"
      reveal
    >
      <q-item class="flex-center">
        <q-item-section class="text-center text-white"
          ><q-item-label class="text-center"
            ><q-btn flat round icon="home" color="white" size="12px" />
            <q-item-label>Home</q-item-label></q-item-label
          ></q-item-section
        >
        <q-item-section class="text-center text-white"
          ><q-item-label class="text-center"
            ><q-btn flat round icon="view_carousel" size="12px" />
            <q-item-label>My Post</q-item-label></q-item-label
          ></q-item-section
        >
        <q-item-section class="text-center"
          ><q-item-label>
            <q-avatar>
              <q-btn
                :icon="'img:/add.png'"
                round
                size="20px"
                class="bg-white text-purple midBtn"
                outline
              /> </q-avatar></q-item-label
        ></q-item-section>
        <q-item-section class="text-center"
          ><q-item-label class="text-center text-white"
            ><q-btn flat round icon="people" size="12px" />
            <q-item-label>Following</q-item-label></q-item-label
          ></q-item-section
        >
        <q-item-section class="text-center"
          ><q-item-label class="text-center text-white"
            ><q-btn flat round icon="person_outline" size="12px" />
            <q-item-label>Profile</q-item-label></q-item-label
          ></q-item-section
        >
      </q-item>
      <!-- <q-tabs active-color="primary"
        indicator-color="transparent"
        no-caps
        class="text-white full-height "
        content-class="layout-tabs">
        <q-route-tab :to="'/home'"
          icon="home"
          label="Home" />
        <q-route-tab :to="{ query: { tab: '1' } }"
          icon="view_carousel"
          label="My Post" />
        <q-route-tab>

        </q-route-tab>
        <q-route-tab to="/following"
          label="Following"
          icon="people" />
        <q-route-tab to="/profile"
          label="Profile"
          icon="person_outline" />
      </q-tabs> -->
    </q-footer>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",
  data() {
    return {
      leftDrawerOpen: false,
      search: null,
      footerNavs: [
        {
          to: "/vehicles",
          label: "Home",
          icon: "home",
        },
        {
          to: "/vehicles",
          icon: "view_carousel",
          label: "My Post",
          // authority: [ADMIN, OM, CSR]
        },
        {
          to: "/trips",
          label: "Following",
          icon: "people",
        },

        {
          to: "/drivers",
          label: "Profile",
          icon: "person_outline",
          // authority: [ADMIN, OM, CO]
        },
      ],
    };
  },
};
</script>

<style scoped>
.iconColor {
  border-radius: 7px;
  color: #42307d;
}

.headerFont {
  font-size: 16px;
  font-weight: 600;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: left;
}

.bgColor {
  background: #42307d;
  border-radius: 0 0 20px 20px;
}

.footer {
  background: #42307d;
  border-radius: 0 0 20px 20px;
  height: 90px;
}

.background-image {
  background-size: cover;
  background-image: url(/bg.png);
  background-size: 100% 100%;
  background-repeat: no-repeat;
}

.midBtn {
  border: 5px solid #42307d;
  margin-top: -40px;
  z-index: 1;
  position: fixed;
}
</style>
