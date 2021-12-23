<template>
  <div class="q-pa-md">
    <q-layout view="hHh Lpr lff" container style="height: 500px; width: 600px" class="shadow-2 rounded-borders">
      <q-header elevated class="bg-teal">
        <q-toolbar>
          <q-btn flat @click="drawer = !drawer" round dense icon="menu"/>
          <q-toolbar-title>Project Bilal</q-toolbar-title>
        </q-toolbar>
      </q-header>

      <q-drawer
          v-model="drawer"
          show-if-above
          :width="200"
          :breakpoint="500"
      >
        <q-scroll-area class="fit">
          <q-list padding class="menu-list">
            <q-item
                :active="activeView === 'dashboard'"
                v-on:click="activeView = 'dashboard'"
                clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="dashboard"/>
              </q-item-section>

              <q-item-section>
                Dashboard
              </q-item-section>
            </q-item>

            <q-item
                :active="activeView === 'speakers'"
                v-on:click="activeView = 'speakers'"
                clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="speaker_group"/>
              </q-item-section>

              <q-item-section>
                Speakers
              </q-item-section>
            </q-item>

            <q-item
                :active="activeView === 'athans'"
                v-on:click="activeView = 'athans'"
                clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="mosque"/>
              </q-item-section>

              <q-item-section>
                Athans
              </q-item-section>
            </q-item>
            <q-separator/>
            <q-item
                :active="activeView === 'settings'"
                v-on:click="activeView = 'settings'"
                clickable v-ripple
            >
              <q-item-section avatar>
                <q-icon name="settings"/>
              </q-item-section>

              <q-item-section>
                Settings
              </q-item-section>
            </q-item>
            <q-item
                :active="activeView === 'help'"
                v-on:click="activeView = 'help'"
                clickable v-ripple
            >
              <q-item-section avatar>
                <q-icon name="help"/>
              </q-item-section>

              <q-item-section>
                Help
              </q-item-section>
            </q-item>
            <q-item
                :active="activeView === 'about'"
                v-on:click="activeView = 'about'"
                clickable v-ripple
            >
              <q-item-section avatar>
                <q-icon name="info"/>
              </q-item-section>

              <q-item-section>
                About
              </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>
      </q-drawer>

      <q-page-container class="bg-teal-2">
        <q-page padding>
          <About v-if="activeView === 'about'"/>
          <Athans v-if="activeView === 'athans'"/>
          <Dashboard v-if="activeView === 'dashboard'"/>
          <Help v-if="activeView === 'help'"/>
          <Settings v-if="activeView === 'settings'"/>
          <Speakers v-if="activeView === 'speakers'"/>
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<script>
import {ref} from 'vue'
import About from "@/components/About";
import Athans from "@/components/Athans";
import Dashboard from "@/components/Dashboard";
import Help from "@/components/Help";
import Settings from "@/components/Settings";
import Speakers from "@/components/Speakers";

export default {
  name: 'app',
  components: {
    About,
    Athans,
    Dashboard,
    Help,
    Settings,
    Speakers
  },
  setup() {
    return {
      activeView: ref('dashboard'),
      athans: ref([]),
      athan: ref(''),
      prayerTimes: ref([]),
      userLocation: ref(null),
      userConfigs: ref(null),
      drawer: ref(false),
    }
  },
  methods: {
    get_athans() {
    },
    get_prayer_configs() {
    },
    get_prayer_times() {
    },
    get_user_configs() {
    },
    get_speakers() {
    },
    set_athan() {
    },
    set_location() {
    },
    set_prayer_configs() {
    },
    set_speaker() {
    },
    set_user_configs() {
    },

  }
}
</script>
