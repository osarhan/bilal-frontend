<template>
  <div>
    <q-page class="flex flex-center text-white">
      <q-card round style="width: 400px; background-color: rgb(0,0,0, 0.25)">
        <q-card-section>
          <div class="text-h6">
            Next Prayer Time
          </div>
          <div class="col text-white q-gutter-md">
            <div class="row text q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-sunset-up"/>
              </div>
              <div class="col-5">
                Fajir
              </div>
              <div class="col-2">
                time
              </div>
            </div>
          </div>
        </q-card-section>
        <q-separator dark/>
        <q-card-section>
          <div class="text-white text-h6">
            Prayer Times
          </div>
          <div class="col text-white q-gutter-md">
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-sunset-up"/>
              </div>
              <div class="col-5">
                Fajir
              </div>
              <div class="col-2">
                time
              </div>
            </div>
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-sunset"/>
              </div>
              <div class="col-5">
                Sunrise
              </div>
              <div class="col-2">
                time
              </div>
            </div>
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-sunny"/>
              </div>
              <div class="col-5">
                Dhuhur
              </div>
              <div class="col-2">
                time
              </div>
            </div>
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-partly-cloudy"/>
              </div>
              <div class="col-5">
                Asr
              </div>
              <div class="col-2">
                time
              </div>
            </div>
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-sunset-down"/>
              </div>
              <div class="col-5">
                Mughrib
              </div>
              <div class="col-2">
                time
              </div>
            </div>
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-weather-night"/>
              </div>
              <div class="col-5">
                Isha
              </div>
              <div class="col-2">
                time
              </div>
            </div>
          </div>
        </q-card-section>
        <q-separator dark/>
        <q-card-section>
<!--          <div class="text-h6">-->
<!--            Athan Active-->
<!--          </div>-->
          <div class="col q-gutter-md">
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-robot"/>
              </div>
              <div class="col-5">
                Athan
              </div>
              <div class="col-2">
                <q-toggle
                    v-model="athanActive"
                    checked-icon="check"
                    color="green"
                    unchecked-icon="clear"
                />
              </div>
            </div>
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-robot"/>
              </div>
              <div class="col-5">
                Fajir Athan
              </div>
              <div class="col-2">
                <q-toggle
                    v-model="fajirActive"
                    checked-icon="check"
                    color="green"
                    unchecked-icon="clear"
                />
              </div>
            </div>
          </div>
        </q-card-section>
        <q-separator dark/>
        <q-card-section>
          <div class="text-h6">
            Athan Speakers
          </div>
          <div class="col q-gutter-md">
            <div class="row q-gutter-md justify-around">
              <div class="col-1">
                <q-icon size="md" name="mdi-google"/>
              </div>
              <div class="col-5">
                Speaker Group Name
              </div>
              <div class="col-2">
                inactive
              </div>
            </div>
          </div>
        </q-card-section>

      </q-card>
    </q-page>
  </div>
</template>

<style>
</style>

<script>
export default {
  name: 'Dashboard',
  data() {
    return {
      'athanActive': true,
      'fajirActive': true
    }
  }
}
</script>
