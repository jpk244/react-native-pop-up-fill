# react-native-pop-up-fill

A cross-platform pop-up-fill component for React Native.

## Installation

```
$ npm install react-native-pop-up-fill --save
```

## Basic Usage

```js
import PopUpFill from 'react-native-pop-up-fill';

// Inside render()
<Prompt
    title="Say something"
    placeholder="Start typing"
    defaultValue="Hello"
    visible={ this.state.promptVisible }
    onSubmit={ (value) => this.setState({
      promptVisible: false,
      message: `You said "${value}"`
    }) }/>
```

## API

Props:

- `visible` (boolean) -- When `true`, the prompt is displayed, closes otherwise
- `title` (string, required) -- The title text of the prompt
- `placeholder` (string) -- The placeholder text of the prompt
- `defaultValue` (string) -- The default value of the prompt
- `onSubmit` (function, required) -- Function that is called with user's value when they submit
- `submitText` (string) -- The string that is displayed on the submit button (defaults to "OK")
- `onChangeText` (function) -- Function that is called with user input when it changes.
- `textInputProps` (Object) -- Additional props on the input element

## Changelog

### 1.0.0

-Cloned and modified react-native-prompt by [@jaysoo](https://github.com/jaysoo) because I did not want a cancel button, but loved the component.
