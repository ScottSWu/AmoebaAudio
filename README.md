AmoebaAudio
===========

Audio visualizer in Javascript using Canvas and Web Audio API

Click to play or pause. Currently supports drag-and-drop for links.

## Usage ##

```
var player = new AmoebaAudio({
	parent : document.getElementById("container")
});

player.load(url); // Must be called first
player.play();
player.pause();
player.toggle();  // Plays if paused or vice versa
player.draw();    // Draws to the generated canvas element added to the parent
```

## Code Outline ##
`new AmoebaAudio`
Creates a new audio player and all relevant dom elements. Appends itself as a child of the parent.
`AmoebaAudio.createMediaElement`
Returns a new `<audio>` element.
`AmoebaAudio.load`
Creates a new audio element and sets up Web Audio nodes.
`AmoebaAudio.draw`
Draws to the canvas. `__draw*` imitate separate layers of the canvas.

## TODO ##
- Support drag-and-drop for files
- Add visibility options (e.g. hide bars at the bottom)
- Allow playlists, drag-and-drop multiple links
