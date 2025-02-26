```html
<template>
  <ion-list>
    <ion-item>
      <ion-select label="Alert" :interface-options="customAlertOptions" interface="alert" placeholder="Select One">
        <ion-select-option value="bacon">Bacon</ion-select-option>
        <ion-select-option value="onions">Onions</ion-select-option>
        <ion-select-option value="pepperoni">Pepperoni</ion-select-option>
      </ion-select>
    </ion-item>

    <ion-item>
      <ion-select
        label="Popover"
        :interface-options="customPopoverOptions"
        interface="popover"
        placeholder="Select One"
      >
        <ion-select-option value="brown">Brown</ion-select-option>
        <ion-select-option value="blonde">Blonde</ion-select-option>
        <ion-select-option value="red">Red</ion-select-option>
      </ion-select>
    </ion-item>

    <ion-item>
      <ion-select
        label="Action Sheet"
        :interface-options="customActionSheetOptions"
        interface="action-sheet"
        placeholder="Select One"
      >
        <ion-select-option value="red">Red</ion-select-option>
        <ion-select-option value="green">Green</ion-select-option>
        <ion-select-option value="blue">Blue</ion-select-option>
      </ion-select>
    </ion-item>

    <ion-item>
      <ion-select label="Modal" :interface-options="customModalOptions" interface="modal" placeholder="Select One">
        <ion-select-option value="reese's">Reese's</ion-select-option>
        <ion-select-option value="snickers">Snickers</ion-select-option>
        <ion-select-option value="twix">Twix</ion-select-option>
      </ion-select>
    </ion-item>
  </ion-list>
</template>

<script>
  import { IonItem, IonLabel, IonList, IonSelect, IonSelectOption } from '@ionic/vue';
  import { defineComponent } from 'vue';

  export default defineComponent({
    components: { IonItem, IonLabel, IonList, IonSelect, IonSelectOption },
    setup() {
      const customAlertOptions = {
        header: 'Pizza Toppings',
        subHeader: 'Select your favorite topping',
        message: 'Choose only one',
        translucent: true,
      };

      const customPopoverOptions = {
        header: 'Hair Color',
        subHeader: 'Select your hair color',
        message: 'Only select your dominant hair color',
      };

      const customActionSheetOptions = {
        header: 'Colors',
        subHeader: 'Select your favorite color',
      };

      const customModalOptions = {
        header: 'Favorite Candy',
        breakpoints: [0, 0.5],
        initialBreakpoint: 0.5,
      };

      return {
        customAlertOptions,
        customPopoverOptions,
        customActionSheetOptions,
        customModalOptions,
      };
    },
  });
</script>
```
