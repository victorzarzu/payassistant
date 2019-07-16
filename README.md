# Tehnologii si labrarii folosite:

[react](https://reactjs.org) -JSX

[react-native](https://facebook.github.io/react-native/) -Mobile app development

[realm](https://realm.io) -Local database

[react-native-background-task](https://github.com/jamesisaac/react-native-background-task) -Background tasks

[react-native-image-pickerhttps://github.com/react-native-community/react-native-image-picker) -Choose the image for the bar code

-react-native-image-view (https://www.npmjs.com/package/react-native-image-view)
•	Pentru a vedea intr-un mod responsive imaginea cu codul de bare
-react-native-vector-icons (https://github.com/oblador/react-native-vector-icons)
•	Pentru a avea la dispozitie iconite specifice
-react-native-svg (https://github.com/react-native-community/react-native-svg)
•	Functionalitatea diagramei
-react-native-chart-kit  (https://www.npmjs.com/package/react-native-chart-kit)
•	Diagrama
-react-navigation (https://reactnavigation.org)
•	Navigare intre componente
-react-native-gesture-handler (https://github.com/kmagiera/react-native-gesture-handler)

# Fotografii folosite care nu imi apartin: 

-buton adaugare factura : https://www.freepik.com/free-icon/round-add-button_778713.htm
-buton pentru a plati toate facturile: https://www.onlinewebfonts.com/icon/281585
-buton stergere factura: https://icons8.com/icon/10657/eliminar-propiedad
-buton platire factura: https://www.freepik.com/free-icon/pay-per-click_754629.htm
-buton pentru a sterge toate facturile: https://www.flaticon.com/free-icon/delete_141966
-buton de navigare inapoi: https://www.freepik.com/free-icon/left-arrow_887187.htm
-background logo: https://www.pngsee.com/m/xbRwx_falling-money-png-money-rain-gif-transparent-png/
-font logo" https://www.dafont.com/third-rail.font?text=PA
-poza barbat profil: https://www.sccpre.cat/show/iTRJwx_male-avatar-icons-png-free-and-downloads-clipart/
-poza femeie profil: https://www.kisspng.com/png-female-avatar-cartoon-clip-art-user-avatar-882481/
-poza unpaid bills home pentru navigatie: https://iconscout.com/icon/product-bill-invoice-purchase-receipt-document-file
-poza paid bills home pentru navigatie: https://iconscout.com/icon/online-site-ecommerce-product-bill-paid-status

# Functii folosite care nu imi apartin

- Functia pentru alegerea timpului de plata pentru Android: 
```
try {
  const {action, hour, minute} = await TimePickerAndroid.open({
    hour: 14,
    minute: 0,
    is24Hour: false, // Will display '2 PM'
  });
  if (action !== TimePickerAndroid.dismissedAction) {
    // Selected hour (0-23), minute (0-59)
  }
} catch ({code, message}) {
  console.warn('Cannot open time picker', message);
}
```
extrasa de pe site-ul: https://facebook.github.io/react-native/docs/timepickerandroid

- Functia pentru alegerea datei de plata pentru Android: 
```
try {
  const {action, year, month, day} = await DatePickerAndroid.open({
    // Use `new Date()` for current date.
    // May 25 2020. Month 0 is January.
    date: new Date(2020, 4, 25),
  });
  if (action !== DatePickerAndroid.dismissedAction) {
    // Selected year, month (0-11), day
  }
} catch ({code, message}) {
  console.warn('Cannot open date picker', message);
}
```
extrasa de pe site-ul: https://facebook.github.io/react-native/docs/datepickerandroid.html

- Functia pentru alegerea datei de plata pentru IOS: 
```
  setDate(newDate) {
    this.setState({chosenDate: newDate});
  }
```
extrasa de pe site-ul: https://facebook.github.io/react-native/docs/datepickerios

- Functia pentru alegerea pozei pentru codul de bare: 
```
ImagePicker.showImagePicker(options, (response) => {
  console.log('Response = ', response);

  if (response.didCancel) {
    console.log('User cancelled image picker');
  } else if (response.error) {
    console.log('ImagePicker Error: ', response.error);
  } else if (response.customButton) {
    console.log('User tapped custom button: ', response.customButton);
  } else {
    const source = { uri: response.uri };

    // You can also display the image using data:
    // const source = { uri: 'data:image/jpeg;base64,' + response.data };

    this.setState({
      avatarSource: source,
    });
  }
});
```

extrasa de pe site-ul: https://github.com/react-native-community/react-native-image-picker
