<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
          <ion-buttons slot="end">
            <ion-button fill="clear" size="small" id="modal1">
              Open Modal
            </ion-button>
          </ion-buttons>
        </ion-toolbar>
      </ion-header>

      <ion-modal ref="modal" trigger="modal1" :initial-breakpoint="1" :breakpoints="[0, 1]" handle="false">
        <div class="wrapper">
          <h1>Title</h1>
          ...
        </div>
      </ion-modal>

      <ExploreContainer name="Tab 1 page" />
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButtons, IonButton, IonModal } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
</script>

<style lang="scss" scoped>
ion-modal {
  --height: auto;

  .wrapper {
    min-height: 20rem;
  }
}
</style>
