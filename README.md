# aframe-stereo-component

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A stereo component for [A-Frame](https://aframe.io) VR.

## Demo
You can see demos for both examples on the [project page](http://oscarmarinmiro.github.io/aframe-stereo-component).

## Features
- **'stereocam' component**: Tells an A-Frame camera which 'eye' to render in case of monoscopic display (without 'Entering VR').
- **'stereo' component**: Tells A-Frame to include an entity in either the 'right' or 'left' eye. Enables stereoscopic video rendering projected on spheres.
- Supports side-by-side equirectangular projection for stereoscopic videos.
- Enables video playback on mobile devices by attaching a 'click' event on the rendering canvas.

## Usage

### Browser Installation

Install and use by directly including the [browser files](dist):

```html
<html>
  <head>
    <script src="https://aframe.io/releases/latest/aframe.min.js"></script>
    <script src="aframe-stereo-component.js.min.js"></script>
  </head>
  <body>
    <a-scene>
      <!-- Example usage -->
      <a-camera position="0 0 10" cursor-visible="false" stereocam="eye:left;"></a-camera>
      <a-entity geometry="primitive: sphere" material="shader: flat; src: #myVideo;" scale="-1 1 1" stereo="eye:left"></a-entity>
      <a-entity geometry="primitive: sphere" material="shader: flat; src: #myVideo;" scale="-1 1 1" stereo="eye:right"></a-entity>
    </a-scene>
  </body>
</html>
```

## License
The MIT License (MIT)