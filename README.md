# react-native-search-bar-animated

React Native SearchBar Component use reanimated library

---

[![CircleCI](https://circleci.com/gh/nghinv-software/react-native-search-bar.svg?style=svg)](https://circleci.com/gh/nghinv-software/react-native-search-bar)
[![Version][version-badge]][package]
[![MIT License][license-badge]][license]
[![All Contributors][all-contributors-badge]][all-contributors]
[![PRs Welcome][prs-welcome-badge]][prs-welcome]

<p align="center">
<img src="./assets/light.gif" width="300"/>
<img src="./assets/dark.gif" width="300"/>
</p>

## Installation

```sh
yarn add react-native-search-bar-animated
```

or 

```sh
npm install react-native-search-bar-animated
```

- peerDependencies

```sh
yarn add react-native-gesture-handler react-native-reanimated
```

## Usage

```js
import React, { useState, useCallback } from 'react';
import { View, Text, StyleSheet } from 'react-native';
import SearchBar from 'react-native-search-bar-animated';

function App() {
  const [text, setText] = useState('');

  const onChangeText = useCallback((value) => {
    setText(value);
  }, []);

  return (
    <View style={styles.container}>
      <SearchBar
        placeholder='Search'
        containerStyle={styles.textInput}
        cancelTitle='Huỷ'
        value={text}
        onChangeText={onChangeText}
        // theme={theme.textInput}
      />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    paddingVertical: 24,
  },
  textInput: {
    marginTop: 40,
    paddingHorizontal: 16,
    paddingVertical: 8,
  },
});

export default App;
```

# Property

| Property | Type | Default | Description |
|----------|:----:|:-------:|-------------|
| containerStyle | `ViewStyle` | `undefined` |  |
| textInputStyle | `TextStyle` | `undefined` |  |
| width | `number \| string` | `undefined` |  |
| height | `number` | `44` |  |
| borderRadius | `number` | `12` |  |
| cancelButton | `boolean` | `true` | Show, hide cancel button |
| cancelTitle | `string` | `Cancel` |  |
| cancelTitleStyle | `TextStyle` | `undefined` |  |
| onFocus | `() => void` | `undefined` |  |
| onBlur | `() => void` | `undefined` |  |
| onSubmitEditing | `() => void` | `undefined` |  |
| value | `string` | `undefined` |  |
| onChangeText | `(value: string) => void` | `undefined` |  |
| isDarkTheme | `boolean` | `false` |  |
| theme | `InputThemeType` |  |  |
| clearIcon | `React.ReactNode` | `null` |  |
| searchIcon | `React.ReactNode` | `null` |  |


- **InputThemeType**

| Property | Type | Default | Description |
|----------|:----:|:-------:|-------------|
| backgroundColor | `string` |  |  |
| placeholderColor | `string` |  |  |
| textInputBackground | `string` |  |  |
| textColor | `string` |  |  |
| selectionColor | `string` |  |  |
| clearIconColor | `string` |  |  |
| textButtonColor | `string` |  | Cancel title color |

```
TextInputThemeDefault = {
  dark: {
    backgroundColor: 'transparent',
    placeholderColor: '#636366',
    textInputBackground: 'rgba(44,44,46,0.8)',
    textColor: 'white',
    selectionColor: '#2979ff',
    clearIconColor: '#c7c7cc',
    searchIconColor: '#b0b0b2',
    textButtonColor: '#2979ff',
  },
  light: {
    backgroundColor: 'transparent',
    placeholderColor: '#8e8e93',
    textInputBackground: 'rgba(142,142,147,0.12)',
    textColor: 'black',
    selectionColor: '#2979ff',
    clearIconColor: '#c7c7cc',
    searchIconColor: '#8e8e93',
    textButtonColor: '#2979ff',
  },
};
```

---
## Credits

- [@Nghi-NV](https://github.com/Nghi-NV)


[version-badge]: https://img.shields.io/npm/v/@nghinv/react-native-search-bar.svg?style=flat-square
[package]: https://www.npmjs.com/package/@nghinv/react-native-search-bar
[license-badge]: https://img.shields.io/npm/l/@nghinv/react-native-search-bar.svg?style=flat-square
[license]: https://opensource.org/licenses/MIT
[all-contributors-badge]: https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square
[all-contributors]: #contributors
[prs-welcome-badge]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
[prs-welcome]: http://makeapullrequest.com
