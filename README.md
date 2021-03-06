# React Native Country Code Picker

## ![npm](https://img.shields.io/npm/l/@digieggs/rn-country-code-picker) ![npm](https://img.shields.io/npm/v/@digieggs/rn-country-code-picker) ![npm](https://img.shields.io/npm/dm/@digieggs/rn-country-code-picker) ![npm](https://img.shields.io/david/DIGIEGGS/rn-country-code-picker)

A searchable dropdown component to select a country code for your phone number input.

<img src="https://github.com/DIGIEGGS/rn-country-code-picker/blob/main/screenshot/picker.gif?raw=true" width="300">

## For Managed Workflow users using Expo

This component is not supported in the managed workflow for expo for the time being.

## Getting started

`npm install @digieggs/rn-country-code-picker --save`

or

`yarn add @digieggs/rn-country-code-picker`

Also you need to manually install `react-native-svg` library for the icons in the component

`npm install react-native-svg --save`

or

`yarn add react-native-svg`

### For react-native@0.60.0 or above

As [react-native@0.60.0](https://reactnative.dev/blog/2019/07/03/version-60) or above supports autolinking, so there is no need to run linking process.
Read more about autolinking [here](https://github.com/react-native-picker/cli/blob/master/docs/autolinking.md).

#### iOS

CocoaPods on iOS needs this extra step

```
npx pod-install
```

#### Android

No additional step is required.

## Usage

First of all, import the component.

```javascript
import { CallingCodePicker } from 'rn-country-code-picker';
```

Then use it like this.

```javascript
const [selectedCallingCode, setSelectedCallingCode] = useState('');

return <CallingCodePicker onValueChange={callingCode => setSelectedCallingCode(callingCode)} />;
```

## Props

- [`initialCountryCode`](#initialCountryCode)
- [`onValueChange`](#onValueChange)
- [`togglerContainerStyle`](#containerStyle)
- [`togglerContainerStyle`](#pickerTogglerLabelStyle)
- [`listContainerStyle`](#listContainerStyle)
- [`searchInputStyle`](#searchInputStyle)
- [`listStyle`](#listStyle)
- [`pickerItemLabelStyle`](#pickerItemLabelStyle)

---

# Reference

## Props

### `initialCountryCode`

the ISO 3166-1 alpha-2 code (FR, US, CA) of the country that you would like to show initially. If you don't pass a value to this, the country code based on your device locale will be used.

| Type   | Required |
| ------ | -------- |
| string | no       |

---

### `onValueChange`

Callback for when a country is selected.

- `callingCode`: the calling code of the selected country

| Type     | Required |
| -------- | -------- |
| function | Yes      |

---

### `togglerContainerStyle`

Style to apply to the toggler container container. (for ex. you can give absolute positioning to align it inside the input.)

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `togglerLabelStyle`

Style to apply to the picker toggler label.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `listContainerStyle`

Style to apply to the list container.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `searchInputStyle`

Style to apply to the search input.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `listStyle`

Style to apply to the FlatList component.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `pickerItemLabelStyle`

Style to apply to each of the item labels.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

## Credits

- https://www.countryflags.io/ (for the flags)
- https://restcountries.eu/ (fetched the info in the countries.json from this api)
