<template>
  <q-layout view="lHh Lpr lFf" class="bg_color">
    <q-header elevated>
      <q-toolbar class="bg-cyan-7">
        <q-item class="logo-padding">
          <q-item-section>
            <q-img
              class="absolute-middle"
              src="../assets/favicon.ico"
              style="height: 40px; width: 40px"
            >
              <q-tooltip class="btn-tooltip">Hyperhire</q-tooltip>
            </q-img>
          </q-item-section>
        </q-item>
        <q-toolbar-title class="no-padding"> Hyperhire </q-toolbar-title>
        <q-space />
        <q-btn-dropdown class="btn-dropdown" stretch flat label="Recruitment">
          <q-list>
            <q-item-label header>Folders</q-item-label>
            <q-item
              v-for="n in 3"
              :key="`x.${n}`"
              clickable
              v-close-popup
              tabindex="0"
            >
              <q-item-section avatar>
                <q-avatar icon="folder" color="secondary" text-color="white" />
              </q-item-section>
              <q-item-section>
                <q-item-label>Photos</q-item-label>
                <q-item-label caption>February 22, 2016</q-item-label>
              </q-item-section>
              <q-item-section side>
                <q-icon name="info" />
              </q-item-section>
            </q-item>
          </q-list>
        </q-btn-dropdown>
        <q-btn
          class="btn_overseas"
          stretch
          flat
          label="overseas developer utilization service"
        />
        <q-space />
        <q-btn
          size="md"
          class="btn_inquiry"
          color="white"
          text-color="primary"
          label="To Inquire"
        />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {},

  data() {
    return {
      leftDrawerOpen: false,
    };
  },

  methods: {
    toggleLeftDrawer() {
      this.leftDrawerOpen = !this.leftDrawerOpen;
    },
  },
});
</script>
<style scoped>
.logo-padding {
  padding: 6px 0px 6px 16px !important;
}
.btn-dropdown {
  text-transform: capitalize !important;
  letter-spacing: 1px !important;
}
.btn_inquiry {
  text-transform: capitalize !important;
}
.btn_overseas {
  text-transform: capitalize !important;
}
.bg_color {
  background-color: rgb(8, 177, 193) !important;
}
@media only screen and (max-width: 700px) {
  /* For desktop: */
  .btn-dropdown {
    display: none !important;
  }
  .btn_inquiry {
    display: none !important;
  }
  .btn_overseas {
    display: none !important;
  }
}
</style>
