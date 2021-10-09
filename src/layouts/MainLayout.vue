<template>
  <q-layout view="lHh Lpr lFf">
    <q-header
      class="bg-white text-grey-10"
      bordered
    >
      <q-toolbar>
        <q-btn
          to="/camera"
          class="q-mr-sm"
          flat
          color="primary"
          icon="eva-camera-outline"
          size="18px"
          dense
        />
        <q-separator
          vertical
          inset
          spaced
        />

        <q-toolbar-title>
          Kaigram
        </q-toolbar-title>
        <q-btn
          to="/"
          flat
          color="primary"
          icon="eva-home-outline"
          size="18px"
          dense
        />
      </q-toolbar>
    </q-header>

    <q-footer
      class="bg-white small-screen-only"
      bordered
    >
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <q-route-tab
          to="/"
          name="home"
          icon="eva-home-outline"
          label="Home"
        />
        <q-route-tab
          to="/camera"
          name="camera"
          icon="eva-camera-outline"
          label="Camera"
        />
      </q-tabs>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',

  data () {
    return {

    }
  }
}
</script>

<style lang="sass">
.q-toolbar
  @media (min-width: $breakpoint-sm-min)
    height: 77px
.q-toolbar__title
  font-size: 30px
  @media (max-width: $breakpoint-xs-max)
    text-align: center
.q-footer
  .q-tab__icon
    font-size: 30px
</style>