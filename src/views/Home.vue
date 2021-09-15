<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Calcula Soma</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <ion-img class="center" alt="soma" width="50px" src="Imagem-calculo.jpg"></ion-img>
      <ion-grid>
        <ion-row>
          <ion-col>
            <ion-label>Número 1 </ion-label>
          </ion-col>
        </ion-row>
        <ion-row>
          <ion-col>
            <ion-input type="number" placeholder="0" v-model="n1"></ion-input>
          </ion-col>
        </ion-row>

        <ion-row>
          <ion-col>
            <ion-label>Número 2: </ion-label>
          </ion-col>
        </ion-row>
        <ion-row>
          <ion-col>
            <ion-input type="text" v-model="n2"></ion-input>
          </ion-col>
        </ion-row>

        <ion-row>
          <ion-col>
            <ion-label>Número 3: </ion-label>
          </ion-col>
        </ion-row>
        <ion-row>
          <ion-col>
            <ion-input type="text" v-model="n3"></ion-input>
          </ion-col>
        </ion-row>

        

        <ion-row>
          <ion-col
            ><ion-button expand="block" @click.prevent="calculo()"
              >CALCULAR</ion-button
            >
          </ion-col>
        </ion-row>

        <ion-row>
          <ion-col>
            <ion-label>Soma: </ion-label>
          </ion-col>
        </ion-row>
        <ion-row>
          <ion-col>
            <ion-input
              type="text"
              v-model="soma"
              placeholder="{}"
              disabled
            ></ion-input>
          </ion-col>
        </ion-row>

      </ion-grid>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
  IonRow,
  IonCol,
  IonButton,
  IonGrid,
  IonImg,
  IonInput,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Home",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonRow,
    IonCol,
    IonButton,
    IonGrid,
    IonImg,
    IonInput,
  },
  data: () => {
    return {
      n1: "",
      n2: "",
      n3: "",
      soma: 0,
    };
  },
  methods: {
    calculo() {
      let x = 0;
      x += parseInt(this.n1);
      x += parseInt(this.n2);
      x += parseInt(this.n3);
      this.soma = x
    },
  },
});
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
.center{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width:200px
}
</style>