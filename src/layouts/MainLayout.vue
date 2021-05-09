<template>
  <q-layout view="lHh Lpr lFf">
    <div class="img-licor">
      <div class="full-width row wrap justify-around items-stretch content-between">
        <div class="q-mt-md">
          <img style="width: 130px;height: 130px;" src="../assets/img/Logo-marrón.png" alt="logo" />
        </div>
      </div>
      <q-header class="bg-transparent">
        <q-toolbar>
          <q-toolbar-title>
          </q-toolbar-title>
          <q-btn class="drawer" flat @click="rightDrawerOpen = !rightDrawerOpen" round dense icon="menu" />
        </q-toolbar>
      </q-header>
      <q-drawer
        side="right"
        v-model="rightDrawerOpen"
        :width="screenDevices"
        show-if-above
        bordered
        content-class="style-drawer img-licor-drawer"
      >
        <q-list padding>
          <q-item-label
            header
            class="text-white row justify-between items-center"
          >
            <div>
              <span></span>
            </div>
            <div style="padding-left: 69px;">
              <span class="text-uppercase" style="font-size: 28px;">Inicio</span>
            </div>
            <div>
              <q-btn flat round icon="close" size="18px" @click="rightDrawerOpen = !rightDrawerOpen" />
            </div>
          </q-item-label>
          <div style="width: 100%;height: 100%;margin-top: 216px;margin-bottom: 241px;font-size: 18px;">
            <EssentialLink
              v-for="link in essentialLinks"
              :key="link.title"
              v-bind="link"
            />
          </div>
        </q-list>
      </q-drawer>
      <Index></Index>
    </div>
    <q-page-container style="padding: 0">
      <FabricationProcess></FabricationProcess>
      <Products></Products>
      <Resource></Resource>
      <Footer></Footer>
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

// const linksData = [
//   {
//     title: 'Docs',
//     caption: 'quasar.dev',
//     icon: 'school',
//     link: 'https://quasar.dev'
//   },
//   {
//     title: 'Github',
//     caption: 'github.com/quasarframework',
//     icon: 'code',
//     link: 'https://github.com/quasarframework'
//   },
//   {
//     title: 'Discord Chat Channel',
//     caption: 'chat.quasar.dev',
//     icon: 'chat',
//     link: 'https://chat.quasar.dev'
//   },
//   {
//     title: 'Forum',
//     caption: 'forum.quasar.dev',
//     icon: 'record_voice_over',
//     link: 'https://forum.quasar.dev'
//   },
//   {
//     title: 'Twitter',
//     caption: '@quasarframework',
//     icon: 'rss_feed',
//     link: 'https://twitter.quasar.dev'
//   },
//   {
//     title: 'Facebook',
//     caption: '@QuasarFramework',
//     icon: 'public',
//     link: 'https://facebook.quasar.dev'
//   },
//   {
//     title: 'Quasar Awesome',
//     caption: 'Community Quasar projects',
//     icon: 'favorite',
//     link: 'https://awesome.quasar.dev'
//   }
// ];

const linksData = [
  {
    title: 'Inicio',
    caption: '',
    icon: '',
    link: '#'
  },
  {
    title: 'Proceso de Fabricación',
    caption: '',
    icon: '',
    link: '#'
  },
  {
    title: 'Productos',
    caption: '',
    icon: '',
    link: '#'
  },
  {
    title: 'Contactos',
    caption: '',
    icon: '',
    link: '#'
  },
];

export default {
  name: 'MainLayout',
  components: {
    EssentialLink,
    Index: ()=> import("../pages/Index"),
    FabricationProcess: ()=> import("../components/FabricationProcess"),
    Products: ()=> import("../components/Products"),
    Resource: ()=> import("../components/Resource"),
    Footer: ()=> import("../components/Footer"),
  },
  created() {
    this.screenDevices = screen.width;
  },
  data () {
    return {
      rightDrawerOpen: false,
      essentialLinks: linksData,
      screenDevices: null
    }
  }
}
</script>

<style scoped>
.img-licor {
  width: 100%;
  background-size: cover;
  background-image:
    linear-gradient(
      rgba(249, 234, 220, 0.7),
      rgba(0, 0, 0, 0.82)
    ),
    url("../assets/img/vegan-wine-club.webp")!important;
  background-repeat: no-repeat;
  background-position: center;
}
.drawer {
  color: #894819!important;
}
</style>
