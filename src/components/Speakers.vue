<template>
  <q-page class="flex flex-center">
    <p>Speakers</p>
    <q-knob
        show-value
        class="text-white q-ma-md"
        v-model="volume"
        size="70px"
        :thickness="0.2"
        color="blue"
        center-color="grey-8"
        track-color="transparent"
    >
      <q-icon name="volume_up"/>
    </q-knob>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'Speakers',
  props: {
    'savedVolume': {
      type: Number,
      default() {
        return 25
      }
    }
  },
  data() {
    return {
      'volume': 25
    }
  },
}
</script>
