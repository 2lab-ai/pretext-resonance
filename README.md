# RESONANCE

Sound shapes text. Every character dances to frequencies.

**[Live Demo](https://2lab-ai.github.io/pretext-resonance/)**

## What

An interactive audiovisual experience where text physically responds to sound. Each character becomes a particle driven by audio frequencies — bass shakes the top rows, mids animate the center, highs ripple the bottom. Your cursor acts as a "sound lens" that amplifies the effect. Click to send ripple waves through the text.

Choose microphone input to see text dance to your voice, or use the built-in procedural synthesizer for an ambient experience.

Built with [pretext](https://github.com/chenglou/pretext) for precise multilingual text measurement and layout.

## Controls

| Input | Action |
|-------|--------|
| Click | Send ripple wave through text |
| Move mouse | Sound lens — amplifies audio near cursor |
| Scroll | Adjust lens radius |
| Space | Pause/resume |
| M | Toggle mic/music |
| ← → | Decrease/increase sensitivity |
| R | Reset all characters |
| 1 / 2 / 3 | Sensitivity presets (low / normal / high) |
| C | Toggle cymatics mode |
| Double tap (mobile) | Pause/resume |
| Pinch (mobile) | Adjust lens radius |

## Audio Engine

The built-in synthesizer generates ambient electronic music in real-time:

- **Sub bass drone** with LFO modulation (55Hz A1)
- **Warm pad** with sawtooth oscillators and filter sweep
- **Chord progression**: Am → Em/G → F → G (cycles every 4 bars)
- **Arpeggio** that follows the current chord
- **Kick drum** pattern (4-on-the-floor with variation)
- **Hi-hat** noise bursts
- **Convolution reverb** for spatial depth
- Click triggers a pitch-drop burst

## Features

- Per-character physics: spring return, velocity-based rotation/scale
- 3 frequency bands (bass/mid/high) mapped to text rows
- Beat detection with expanding ring animations
- Word group highlighting on each beat
- Sound lens cursor: chars near mouse react more strongly
- Click ripple: expanding ring pushes characters outward
- Constellation lines between energetic characters
- Circular spectrum visualizer (center)
- Linear spectrum bar (bottom)
- Waveform overlay
- Audio-reactive background color
- Starfield with audio-responsive twinkling
- Idle breathing animation (active without audio)
- Mic input with gain normalization + dynamics compressor
- Full touch support (tap, drag, pinch, double-tap)

## Tech

Single `index.html` — no build step:

```js
import { prepareWithSegments, layoutNextLine } from 'https://esm.sh/@chenglou/pretext@0.0.3'
```

Web Audio API for all synthesis, analysis, and effects. Canvas 2D for rendering.

## The Science of Resonance

Resonance is the phenomenon where two objects with the same natural frequency amplify each other's vibrations. In this visualization, your voice or the synthesizer's frequencies physically move text characters — bass frequencies shake the top rows with large amplitude, while high frequencies create subtle tremors in the bottom rows. Each character has a unique phase offset, creating wave patterns that emerge from the collective motion.

## Credits

- [pretext](https://github.com/chenglou/pretext) by chenglou — text measurement & layout
- Built by [2lab.ai](https://github.com/2lab-ai)
