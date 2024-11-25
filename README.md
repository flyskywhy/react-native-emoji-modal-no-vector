# react-native-emoji-modal-no-vector

[![npm version](http://img.shields.io/npm/v/react-native-emoji-modal-no-vector.svg?style=flat-square)](https://npmjs.org/package/react-native-emoji-modal-no-vector "View this project on npm")
[![npm downloads](http://img.shields.io/npm/dm/react-native-emoji-modal-no-vector.svg?style=flat-square)](https://npmjs.org/package/react-native-emoji-modal-no-vector "View this project on npm")
[![npm licence](http://img.shields.io/npm/l/react-native-emoji-modal-no-vector.svg?style=flat-square)](https://npmjs.org/package/react-native-emoji-modal-no-vector "View this project on npm")
[![Platform](https://img.shields.io/badge/platform-ios%20%7C%20android-989898.svg?style=flat-square)](https://npmjs.org/package/react-native-emoji-modal-no-vector "View this project on npm")

> Feature-complete emoji picker for React Native that mimics the look and feel of native ones.

[react-native-emoji-modal](https://github.com/staltz/react-native-emoji-modal) is a rewrite of [react-native-emoji-picker](https://github.com/staltz/react-native-emoji-picker-staltz).

`react-native-emoji-modal-no-vector` replace `react-native-vector-icons` with easier installing `react-native-svg` base on [react-native-emoji-modal](https://github.com/staltz/react-native-emoji-modal).

![screenshot](./screenshot.png)

**Features:**

- Vertically scrolling with 7 columns of emoji
- Search field
- Category shortcuts
- Supports iOS
- Supports Android
  - It's aware of Android versions and their availability of emojis
  - Except for category shortcuts (PRs welcome to fix this!)
- Written in TypeScript
- Lightweight
  - Loads just 163 kB worth of emoji data, versus 1.2 MB in react-native-emoji-picker

## Installation

```bash
npm install --save react-native-emoji-modal-no-vector
```

## Usage

```jsx
import EmojiModal from 'react-native-emoji-modal-no-vector';

// ...

<EmojiModal onEmojiSelected={(emoji) => {}} />;
```

## Props

| Prop name             | Description                                                           | Type          | Required | Default                                                                                                                                      |
| --------------------- | --------------------------------------------------------------------- | ------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `onEmojiSelected`     | Function called when the user presses one of the emojis shown         | function      | true     |                                                                                                                                              |
| `onPressOutside`      | Function called when the user taps outside of the emoji picker region | function      | false    |                                                                                                                                              |
| `columns`             | How many columns of emojis to render in the grid                      | number        | false    | 7                                                                                                                                            |
| `localizedCategories` | Customize the labels for each category                                | Array<string> | false    | `['Smileys & Emotion', 'People & Body', 'Animals & Nature', 'Food & Drink', 'Activities', 'Travel & Places', 'Objects', 'Symbols', 'Flags']` |
| `emojiSize`           | Customize the size of each emoji, in pixels                           | number        | false    | 32                                                                                                                                           |
| `emojiStyle`          | Custom style for each emoji                                           | TextStyle     | false    |                                                                                                                                              |
| `headerStyle`         | Custom style for the label for each category                          | TextStyle     | false    |                                                                                                                                              |
| `scrollStyle`         | Custom style for the FlatList with the grid of emojis                 | ViewStyle     | false    |                                                                                                                                              |
| `searchStyle`         | Custom style for the search TextInput                                 | ViewStyle     | false    |                                                                                                                                              |
| `shortcutColor`       | Color for inactive category shortcuts                                 | color         | false    | `#bcbcbc`                                                                                                                                    |
| `activeShortcutColor` | Color for the active category shortcut                                | color         | false    | `#0c0c0c`                                                                                                                                    |
| `containerStyle`      | Custom style for the "box" in the center                              | ViewStyle     | false    |                                                                                                                                              |
| `backgroundStyle`     | Custom style for the background of the modal                          | ViewStyle     | false    |                                                                                                                                              |
| `modalStyle`          | Custom style for top-level container                                  | ViewStyle     | false    |                                                                                                                                              |
| `blockfuncEmojis`     | Function to block emojis, e.g. `emoji => {return /1F...-1F.../.test(emoji.unified);}` | function      | false    |                                                                                                                                              |

## Support us!

This library was created for [Manyverse](https://manyver.se) and we're very thankful for our [backers on OpenCollective](https://opencollective.com/manyverse), and we need more donations! :pray:

## License

[MIT](LICENSE)
