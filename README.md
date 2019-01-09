<p align="center">
  <a href="https://github.com/matvp91/indigo-player">
    <img align="center" src="https://raw.githubusercontent.com/matvp91/indigo-player/master/docs/indigo-player.png">
  </a>
</p>

# indigo-player

Highly extensible, modern, JavaScript player.

[![](https://img.shields.io/npm/v/indigo-player.svg)](https://www.npmjs.com/package/indigo-player)
[![](https://img.shields.io/github/license/matvp91/indigo-player.svg)](https://github.com/matvp91/indigo-player)
[![](https://img.shields.io/snyk/vulnerabilities/github/matvp91/indigo-player.svg)](https://github.com/matvp91/indigo-player)
[![](https://img.shields.io/npm/types/indigo-player.svg)](https://www.npmjs.com/package/indigo-player)

**Important:** This package is under construction and although it offers a fair amount of features already, this is a work in progress. At the moment, it lacks the proper documentation but with time comes improvement.

## Features

* Fluid mp4 playback.
* Support for Dash (+ DRM / Widevine & PlayReady). - *shaka-player*
* Support for HLS. - *hls.js*
* Advertisement support with FreeWheel.
* A modular structure that allows any developer to hook into the player logic and write custom business rules and extensions. Basically the entire player structure is built as a set of modules.
* Bundle splitting, only loads JS files (eg: HLS.js) when actually needed.

**Note:** Native HLS (+ FairPlay) is a work in progress

## Documentation

Visit the [documentation](https://matvp91.github.io/indigo-player).

## Getting started

The example below will load a simple MP4 file, and attempt to autoplay it.

```javascript
<html>
  <body>
    <script src="https://unpkg.com/indigo-player/lib/indigo-player.js"></script>
    const config = {
      autoplay: true,
      sources: [
        {
          type: 'mp4',
          src: 'https://samples.com/BigBuckBunny.mp4',
        },
      ],
    };

    const element = document.getElementById('player');
    const player = IndigoPlayer.init(element, config);
    
    // You can use the player object now to access the player and it's methods (play, pause, ...)
  </body>
</html>

```
