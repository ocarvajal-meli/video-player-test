# Capabilities Video Player (beta)

- Controles de reproducción (stop, play & pause): Mostrar controles básicos de reproducción.

```jsx
<VideoPlayer controls />
```
- FF y RF: Controles para aumentar o disminuir la velocidad de la reproducción.

```jsx
<VideoPlayer forward={true} />
```
- Start over: Mostrar botón para reiniciar la reproducción del contenido.

```jsx
<VideoPlayer startOver={true} />
``` 
- Thumbnail Scrubber: Mostrar thumbnail en la barra de progreso de la reproducción donde se interactúe con ella.

```jsx
<VideoPlayer thumbnailScrubber={true} />
``` 
- Subtítulos multi-idioma: (?)

```jsx
<VideoPlayer ? />
``` 
- Audio multi-idioma: (?)

```jsx
<VideoPlayer ? />
``` 
- Tipo de media: (?)

```jsx
<VideoPlayer media="movie" />
``` 

## Implementación de ejemplo

```jsx
<VideoPlayer

    mediaType: string = "movie" // show custom control for each media type ('movie' | 'show')
    continousPlay: boolean = {true} // default false

    controls: Object = {
        enablePlayButton: boolean, // default: true
        enablePauseButton: boolean, // default: true
        enableStopButton: boolean, // default: false
        enablePlaybackSpeedControls: boolean, // default: false
        adsControls: {
            skipAdsAfterXSec: integer, // Represent time by seconds (default: 5)
        },
        tvShowControls: {
            skipIntroButton: boolean, // default: true,
            nextEpisodeButton: boolean, // show next episode button on the end of actual episode (default: false)
            showEpisodeNavigationButton: boolean, // show buttons to navigate to past and next episode (default: true)
        }
    }
/>
```

## Callbacks

```jsx
<VideoPlayer
    ...controls
    
    onStop={handleFunction}
/>
```