---
name: 'Video: Edit'
description: Choose this template when it's time to edit a video.
about: Choose this template when it's time to edit a video.
title: 'Edit: [video_name]'
labels: ''
assignees: ''

---

## Video

### Video: Software

- [Kdenlive](https://kdenlive.org/) (for all platforms)
- [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve) (for Windows & Mac)
- [Final Cut Pro](https://www.apple.com/final-cut-pro/) (for Mac)

### Video: Hardware

- A laptop/desktop.

### Video: Edit steps

Regardless of the software used, I tend to always have the same framework:

1. Import and sort all media
2. Create a timeline for each section of the video, and a main timeline.
3. Edit a rough-cut within each timeline.
4. Finalize all timelines.
5. Merge all timelines in the main timeline, and finalize the video.
6. Export.

## Audio

### Audio: Edit steps

When editing audio such as a voice-over, I have tried different steps in different orders, but this is what I find is the best (most of the times):

1. Rough manual normalization (drag down the highest peaks)
2. EQ (apply in following order)
    1. Low rolloff for voice (drop low-end from 100 Hz)
    2. Bass boost (boost from 600 Hz (0 db) to 100 Hz (3 db))
    3. Treble boost (boost from 4000 Hz (0 db) to 5000 Hz (3 db))
3. Compressor (real-time effect)
    - Choose `Podcast/Radio` preset and adjust Make-up gain (Threshold: -15; Make-up gain: 0; Knee-width: 24; Ratio: 3; Lookahead: 1; Attack (ms): 15; Release (ms): 40)
4. Limiter (real-time effect)
    - Choose `VO Limiter` (Threshold: -4; Make-up gain target: -1; Knee width: 0; Lookahead (ms): 0.1; Release (ms): 10.1)
5. Normalizer (optionally)
    - If the compressor and limiter has done it's job, you don't need the limiter. But in cases you still need to bump up the audio to be nearer 0 db at peaks, first mix the track (Tracks -> Mix -> Mix and Render), and then apply the normalizer with it set to -1 db.
6. Export
