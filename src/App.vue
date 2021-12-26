<template>
  <div>
    <q-layout
        style=" background: linear-gradient(teal 50%, #0c70e5 100% )"
        class="shadow-2 ">
      <q-header
          elevated
          class="bg-teal">
        <q-toolbar>
          <q-btn
              flat
              @click="drawer = !drawer"
              round
              dense
              icon="menu"
          />
          <q-toolbar-title>
            Project Bilal
          </q-toolbar-title>
        </q-toolbar>
      </q-header>

      <q-drawer
          v-model="drawer"
          show-if-above
          :width="190"
          :breakpoint="500"
      >
        <q-list padding class="menu-list">
          <div
              v-for="m in menuItems"
              :key="m">
            <q-item
                :active="activeView === m"
                v-on:click="changeView(m)"
                clickable
                v-ripple>
              <q-item-section avatar>
                <q-icon :name="m === 'Athans' ? 'mosque' : m.toLowerCase()"/>
              </q-item-section>
              <q-item-section>
                {{ m }}
              </q-item-section>

            </q-item>
            <q-separator v-if="m === 'Speakers'"/>
          </div>

        </q-list>
        <q-chip>Made by Omar and Rafik</q-chip>
      </q-drawer>

      <q-page-container>
        <About v-if="activeView === 'Info'"/>
        <Athans v-if="activeView === 'Athans'"/>
        <Dashboard v-if="activeView === 'Dashboard'"/>
        <Help v-if="activeView === 'Help'"/>
        <Settings v-if="activeView === 'Settings'"/>
        <Speakers v-if="activeView === 'Speakers'"/>
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
      menuItems: ['Dashboard', 'Athans', 'Speakers', 'Settings', 'Help', 'Info']
    }
  },
  methods: {
    changeView(newView) {
      this.activeView = newView
      this.drawer = false
    },
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
