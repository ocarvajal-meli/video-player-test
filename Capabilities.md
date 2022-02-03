# Capabilities Video Player (beta)

This is a beta version of properties and callbacks for Vide Player lib. This document and all references is a representation of capabilities document (v2) that you can [found here](https://docs.google.com/spreadsheets/d/1cTfCN22kgeVNxZx4NHTBum6h4h5W6KMvEHOsicwDNPs/)
## Example with properties

```jsx
<VideoPlayer

    mediaType: string = "movie" // show custom control for each media type / ('movie' | 'show')
    continousPlay: boolean = {true} // default: false
    thumbnailScrubber: boolean = {true} // show thumbnails on top of progress bar / default: false

    // control properties
    enablePlayButton: boolean, // default: true
    enablePauseButton: boolean, // default: true
    enableStopButton: boolean, // default: false
    enablePlaybackSpeedControls: boolean, // default: false
    enableStartOver: boolean, // default: false
    adsControls: {
        skipAdsAfterXSec: integer, // Represents time in seconds (default: 5)
    },
    tvShowControls: {
        skipIntroButton: boolean, // default: true,
        nextEpisodeButton: boolean, // show next episode button on the end of actual episode / default: false
        showEpisodeNavigationButton: boolean, // show buttons to navigate to past and next episode / default: true
    }
/>
```

## Example with callbacks

```jsx
<VideoPlayer
    ...controls
    
    onStop={handleFunction} // triggered when stop reproduction event has been dispatched
/>
```