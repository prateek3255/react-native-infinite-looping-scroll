# react-native-infinite-looping-scroll

A react native component that lets you scroll infinitely in both directions by repeating the same items.

<p align="center">
<img src="https://drive.google.com/uc?id=1Uy7QNttuQ_f45U2oan4MWBivae4Xsj2S" width="200" height="400">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://drive.google.com/uc?id=1re6VhBZ8NZIsPYvN5DMhgveA7ei87N9U" width="200" height="400">
</p>

## Installation

Run `npm install react-native-infinite-looping-scroll` in your project directory.

## Usage

This snippet would produce the output shown in the above gif

```
import React, { Component } from 'react';
import { Platform, StyleSheet, Text, View, FlatList, } from 'react-native';
import InfiniteScroll from 'react-native-infinite-looping-scroll';


export default class App extends Component {
  constructor(props) {
    super(props)
  }
 
  render() {
    return (
      <View style={styles.container}>
        <InfiniteScroll
        data={[{ key: '1' }, { key: '2' }, { key: '3' }, { key: '4' }, { key: '5' }, { key: '6' }, { key: '7' }]}
        renderItem={({ item }) => <View style={styles.listItem}><Text>{item.key}</Text></View>}
        />
        
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  listItem: {
    flexDirection: 'row',
    justifyContent: 'space-between',
    alignItems: 'center',
    padding: 50,
    margin: 2,
    borderColor: '#2a4944',
    borderWidth: 1,
    backgroundColor: '#d2f7f1'
  },
  welcome: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
  instructions: {
    textAlign: 'center',
    color: '#333333',
    marginBottom: 5,
  },
});

```

## Props

It accepts all the [FlatList](https://facebook.github.io/react-native/docs/flatlist.html) props out of which renderItem and data are the compulsory ones and has one more extra prop called `offset` which lets you set the offset at which new data should be added. The default value is 20 and you can change it according to your item.

## Pending Tasks

- [ ] Make upward and downward scroll more smooth.
- [ ] The scroll view should work even when the content size is less than the layout measurement.

## Contributing

This is project is still in beta at the moment, but is still very basic, so if you want to work on the above mention tasks, or you find a bug just open a PR or an issue and ping me!
