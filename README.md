# cloudinary-video-player

## Installation

### NPM
1. Install the files using:

   ```shell
   npm install lodash cloudinary-core cloudinary-video-player
   ```
1. Include the javascript file in your HTML. For Example:

   ```html
   <link href="node_modules/cloudinary-video-player/dist/cld-video-player.min.css" rel="stylesheet">

   <script src="node_modules/lodash/lodash.js" type="text/javascript"></script>
   <script src="node_modules/cloudinary-core/cloudinary-core.js" type="text/javascript"></script>
   <script src="node_modules/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>
   ```

### CDN

Cloudinary Video Player can also be included directly from the [Unpkg CDN](https://unpkg.com/#/):

```html
<link href="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css" rel="stylesheet">

<script src="https://unpkg.com/cloudinary-core/cloudinary-core-shrinkwrap.min.js" type="text/javascript"></script>
<script src="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>
```

### Packages

The Cloudinary video player offers standard and light package variations, available in either minified or non-minified formats.
* Standard package: Includes all functionality described in this video player [documentation](https://cloudinary.com/documentation/cloudinary_video_player).  
* Light package: Excludes the following optional functionality: Adaptive bitrate streaming (HLS and MPEG-DASH), Video ads, Shoppable videos (alpha)  

- `cld-video-player.js` - Non minified version which includes all optional modules.
- `cld-video-player.min.js` - Minified version which includes all optional modules.
- `cld-video-player.light.js` - Non minified version which does not include any optional modules.
- `cld-video-player.light.min.js` - Minified version which does not include any optional modules. (for smaller bundle size)

#### Adaptive Streaming

- HLS is supported out of the box in both standard and light packages. To use an m3u8 as the video source, you can specify sourceTypes=['hls'].

- MPEG-DASH support:
Is enabled by specifying sourceTypes=['dash'] for your video source.

- MPEG-DASH dependencies:
For version 1.4.0 and higher: MPEG-DASH dependencies are already included in the standard package.  
For older versions, or if using the light package: to use MPEG-DASH files in your video player, include the following files in addition to the files described above:

```javascript
<script src="https://cdnjs.cloudflare.com/ajax/libs/dashjs/3.0.2/dash.all.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/videojs-contrib-dash/2.11.0/videojs-dash.min.js" type="text/javascript"></script>
```

### Cloudinary JavaScript library

The Core Cloudinary JavaScript library provides several classes, defined under the "`cloudinary`" domain. The reference documentation is located at https://cloudinary.github.io/pkg-cloudinary-core

#### Getting started

Create a video tag containing `cld-video-player` class and a supported skin class:
```html
<video
  id="example-player"
  controls
  autoplay
  data-cld-public-id="dog"
  class="cld-video-player cld-video-player-skin-dark">
</video>
```

Instantiate a new `cloudinary.Cloudinary` instance containing your cloudinary configuration:

```javascript
var cld = cloudinary.Cloudinary.new({ cloud_name: "demo"});
```

Instantiate a new cloudinary Video Player:
```javascript
cld.videoPlayer('example-player')
```

#### Documentation
- [Documentation](https://cloudinary.com/documentation/cloudinary_video_player)
- [API Reference](https://cloudinary.com/documentation/video_player_api_reference)
- [Demo](https://demo.cloudinary.com/video-player/)
- [Code Examples](https://cloudinary.github.io/cloudinary-video-player/)
- [Video Player Studio](https://studio.cloudinary.com/) 

#### Development
In order to run this project locally:
1. [Install yarn](https://yarnpkg.com/lang/en/docs/install/)
1. Clone this repository
1. `yarn install`
1. `yarn start`
