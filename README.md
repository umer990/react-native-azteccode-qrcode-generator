# react-native-azteccode-qrcode-generator
A react-native component to generate [AztecCode](http://members.chello.at/easyfilter/barcode.js) and [QRcode](http://en.wikipedia.org/wiki/QR_code) , not only support English.

## this module support iOS and Android

## Installation
```sh
npm install https://github.com/umer990/react-native-azteccode-qrcode-generator/tarball/master --save-dev
```
## Usage
```jsx
'use strict';

import React, { Component } from 'react'
import code from 'react-native-azteccode-qrcode-generator';

Aztec=code.Aztec;
QRCode=code.QRCode;

import {
    AppRegistry,
    StyleSheet,
    View,
    TextInput
} from 'react-native';

class HelloWorld extends Component {
  state = {
    text: 'react-native-azteccode-qrcode',
  };

  render() {
    return (
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          onChangeText={(text) => this.setState({text: text})}
          value={this.state.text}
        />
        <QRCode
          value={this.state.text}
          size={200}
          bgColor='purple'
          fgColor='white'/>
        <Text style={styles.welcome}>
          Aztec Example
        </Text>
         <Aztec
          value={this.state.text}
          size={200}
          bgColor='black'
          fgColor='white'/>
      </View>
    );
  };
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        backgroundColor: 'white',
        alignItems: 'center',
        justifyContent: 'center'
    },
    welcome: {
        fontSize: 20,
        textAlign: 'center',
        margin: 10,
      },
    input: {
        height: 40,
        borderColor: 'gray',
        borderWidth: 1,
        margin: 10,
        borderRadius: 5,
        padding: 5,
    }
});

AppRegistry.registerComponent('HelloWorld', () => HelloWorld);

module.exports = HelloWorld;
```
## Available Props

prop      | type                 | default value
----------|----------------------|--------------
`value`   | `string`             | `http://facebook.github.io/react-native/`
`size`    | `number`             | `128`
`bgColor` | `string` (CSS color) | `"#FFFFFF"`
`fgColor` | `string` (CSS color) | `"#000000"`

<img src='qrcode.png' height = '256' width = '256'/>

