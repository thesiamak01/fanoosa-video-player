# Fanoosa Video Player

![Banner](https://raw.githubusercontent.com/thesiamak01/fanoosa-video-player/refs/heads/main/cover.png)

Fanoosa Video Player is a lightweight, customizable, and responsive HTML5 video player built with JavaScript and CSS. It provides a simple and elegant solution for embedding videos on your website with a variety of controls and features.

## Features

- **Customizable Controls**: Play/Pause, Volume, Fullscreen, Speed Control, Progress Bar, and Center Play/Pause button.
- **Responsive Design**: Works seamlessly on both desktop and mobile devices.
- **Video Ad**: Play an ad before loading the main video (with a skip option, defaulting to 5 seconds after playback).
- **Video Cards**: Display interactive cards at specific timestamps during video playback.
- **Keyboard Shortcuts**: Control playback using keyboard shortcuts (e.g., Space, Arrow Keys, etc.).
- **Loading Spinner**: Displays a loading spinner while the video is buffering.
- **Fullscreen Mode**: Supports fullscreen mode with automatic landscape orientation on mobile devices.
- **Customizable Settings**: Easily configure the player's behavior via a JavaScript configuration object.

## Installation

To use Fanoosa Video Player in your project, simply include the necessary CSS and JavaScript files in your HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fanoosa Video Player</title>
   
    <link href="FanoosaVideoPlayer.min.css" rel="stylesheet" type="text/css">
   <script src="FanoosaVideoPlayer.min.js" type="text/javascript"></script>
</head>
<body>
    <div id="video-container">
        <video id="FVideoPlayer" poster="thumbnail.png">
            <source src="video.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
        <video id="FVideoPlayerAd">
          <source src="ad.mp4" data-link="https://example.com" data-title="example" type="video/mp4">
        </video>
        <div id="video-cards">
            <a href="#" class="FVideoPlayerCard" target="_blank" data-card-time="00:10">Visit Our Website</a>
            <a href="#" class="FVideoPlayerCard" target="_blank" data-card-time="00:65">Support</a>
            <a href="#" class="FVideoPlayerCard" target="_blank" data-card-time="01:20:01">Buy Package</a>
        </div>
    </div>

    <script>
        const config = {
            videoContainerId: 'video-container',
            controls: {
                playPause: true,
                volume: true,
                fullscreen: true,
                speed: true,
                progressBar: true,
                centerPlayPause: true
            },
            defaultVolume: 1,
            defaultSpeed: 1,
            speedOptions: [0.5, 1, 1.5, 2],
            hideControlsTimeout: 1000,
            showCards: true,
            hideCardsTimeout: 5000,
            adConfig: {
              showAd: true,
              adCountdownDuration: 5,
            }
        };

        const player = new VideoPlayer(config);
    </script>
</body>
</html>
```
## Configuration
The player can be customized using the following configuration options:

- **videoContainerId**: The ID of the container element for the video player.


- **controls**: An object to enable or disable specific controls:

  - **playPause**: Show/hide the play/pause button.

  - **volume**: Show/hide the volume control.

  - **fullscreen**: Show/hide the fullscreen button.

  - **speed**: Show/hide the speed control.

  - **progressBar**: Show/hide the progress bar.

  - **centerPlayPause**: Show/hide the center play/pause button.

   
- **defaultVolume**: Set the default volume level (0 to 1).

- **defaultSpeed**: Set the default playback speed.

- **speedOptions**: Array of available playback speed options.

- **hideControlsTimeout**: Time in milliseconds before the controls are hidden.

- **showCards**: Enable/disable video cards.

- **hideCardsTimeout**: Time in milliseconds before the video cards are hidden.


- **adConfig**: These settings control the behavior of ads in the video player.
  - **showAd**: Enable/disable ads before or during the video.
  - **adCountdownDuration**: Duration (in seconds) before the ad can be skipped.

## Keyboard Shortcuts

- **Space**: Play/Pause

- **F**: Toggle Fullscreen

- **Arrow Right**: Skip forward 5 seconds

- **Arrow Left**: Skip backward 5 seconds

- **Arrow Up**: Increase volume

- **Arrow Down**: Decrease volume

- **M**: Mute/Unmute


## Contributing
Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Author
   - `Siamak Yousefi`


Enjoy using Fanoosa Video Player! If you find it useful, consider giving it a ⭐️ on GitHub!