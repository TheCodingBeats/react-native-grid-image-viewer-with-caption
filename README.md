# react-native-grid-image-viewer-with-caption
A grid display for multiple images with caption which you can view on clicking in fullscreen mode and swipe through.

## Key Points

* Grid Image Viewer With Caption
* Full Screen Mode Image Viewer
* Max Lightweight Component
* No Dependency, No Configuration
* Click on image to view full screen
* Smooth Animation
* Swipe image to navigate to next image
* Available for iOS and Android
* Also works with Expo

## Installation

```
npm i react-native-grid-image-viewer-with-caption --save
```

### or

```
yarn add react-native-grid-image-viewer-with-caption
```
## Usage

#### Class component

```js
import React from 'react';
import { View, StyleSheet, Text } from 'react-native';
import GridImageViewerCaption from 'react-native-grid-image-viewer-with-caption';

export default class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      gallery:[
        { image: 'http://image.jpg', text:'Caption 1' },
        { image: 'http://image.jpg', text:'Caption 2' },
        { image: 'http://image.jpg', text:'Caption 3' }
      ]
    };
  }

  render() {
    return (
       <View style={styles.background}>
      <Text style={styles.headline_text}>Grid View Images With Caption</Text>
      <Text style={styles.explore_text}>Click on an image to view in full screen mode</Text>

      <GridImageViewerCaption data={this.state.gallery} captionColor="#fff" />
    </View>
    );
  }
};

const styles = StyleSheet.create({
  background: {
    backgroundColor: 'black',
    flex: 1
  },
  headline_text: {
    color: 'white',
    fontSize: 30,
    fontWeight: 'bold',
    marginTop: 50,
    marginLeft: 20
  },
  explore_text: {
    marginTop: 5,
    marginBottom: 10,
    color: 'white',
    marginLeft: 20,
    fontSize: 12,
    fontWeight: '600'
  },
});
```


## Props

| Prop            | Type     | Description                                             |
| ---------------- | -------- | ------------------------------------------------------- |
| data    | array  | List of images to be displayed in the grid should be in the form: [{image: url1}, {image: url2}, ...] |
| headers    | json  | (Optional) Pass headers, for instance to restrict access. Eg. {'Authorization': 'Bearer ' + 'TOKEN'} |
| renderGridImage    | function(item, defaultStyle) => Node  | (Optional) Custom function to render each image in grid view. Default style must be applied on the returned node and the image itself (if different). |
| renderModalImage    | function(item, defaultStyle) => Node  | (Optional) Custom function to render each image in modal view. Default style must be applied on the <Image /> node. |
| transparent    | int  | (Optional) Transparency on the background when single image is viewed in full screen mode, Range=[0, 1] |
| Caption Color    | string  | (Optional) (Default = white) Change the caption color by ading, captionColor="color" |

## License

This project is licensed under the MIT License - see [LICENSE.md](https://github.com/TheCodingBeats/react-native-grid-image-viewer-with-caption/blob/main/LICENSE) for details


## Author

Made by [The Coding Beats](https://github.com/TheCodingBeats)
