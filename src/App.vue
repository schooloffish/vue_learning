<template>
  <v-app>
    <!--// <v-app-bar app color="primary" dark>
    //   <div class="d-flex align-center">
    //     <v-img
    //       alt="Vuetify Logo"
    //       class="shrink mr-2"
    //       contain
    //       src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
    //       transition="scale-transition"
    //       width="40"
    //     />

    //     <v-img
    //       alt="Vuetify Name"
    //       class="shrink mt-1 hidden-sm-and-down"
    //       contain
    //       min-width="100"
    //       src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
    //       width="100"
    //     />
    //   </div>

    //   <v-spacer></v-spacer>

    //   <v-btn
    //     href="https://github.com/vuetifyjs/vuetify/releases/latest"
    //     target="_blank"
    //     text
    //   >
    //     <span class="mr-2">Latest Release</span>
    //     <v-icon>mdi-open-in-new</v-icon>
    //   </v-btn>
    // </v-app-bar> -->

    <v-content>

      <Drawer />
      <div style="margin-left:100px;">
        <v-breadcrumbs :items="items">
          <template v-slot:item="props">
            <a>{{props.item.text}}</a>
          </template>
        </v-breadcrumbs>
        <FlowDesign />
      </div>
      
    </v-content>
  </v-app>
</template>

<script>
import Drawer from "./components/Drawer";
import FlowDesign from "./components/FlowDesign";

export default {
  name: "App",

  components: {
    Drawer,
    FlowDesign
  },

  data: () => ({
    items:[
      {
        text:'首页'
      },
      {
        text:'流程编排'
      },
      {
        text:'模块流程编排'
      }
    ]
  })
};
</script>
