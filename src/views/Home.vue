<template>
<ion-app>
    <router-view></router-view>
  </ion-app>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar color="primary">
        <ion-buttons slot="start">
          <ion-menu-button auto-hide="false" class="ion-margin-end" componentId="main" @click="openStart()"></ion-menu-button>

            <ion-button>
      <ion-icon  name="search"></ion-icon>
    </ion-button>
    
        </ion-buttons>
        
        <ion-title>Blank Project</ion-title>

        <ion-buttons slot="end">
          <ion-button>
          <ion-icon  name="cart"></ion-icon>
          </ion-button>
          </ion-buttons>
      </ion-toolbar>
    </ion-header>
    
    <ion-content>
      <ion-item >
        <ion-label>Label 1</ion-label>
        <ion-label>Label 2</ion-label>
        <ion-label>Label 3</ion-label>
      </ion-item>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
//import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
//import { defineComponent } from 'vue';
import Subcomponent from '@/component/Subcomponent.vue';
import { Plugins } from '@capacitor/core';
import {createRouter} from '@ionic/vue-router'

export default {
  name: 'Home',
  methods: {
    openStart () {
      this.$router.push("/Subcomponent");
    }
  }
}


</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}
#container strong {
  font-size: 20px;
  line-height: 26px;
}
#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}
#container a {
  text-decoration: none;
}
</style>