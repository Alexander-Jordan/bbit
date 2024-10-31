# Audio For Videos

## Table of content

- [Tools](#tools)
    - [Software](#software)
    - [Hardware](#hardware)
- [Audio levels](#audio-levels)
    - [Recording](#recording)
    - [Editing](#editing)
- [Edit steps](#edit-steps)

# Tools

## Software

I like software that is accessible, powerfull, simple, and well supported (open-source is a big plus!).

What I end up using the most is [Audacity](https://www.audacityteam.org/), which is available on most platforms, is powerfull yet simple, and it has a big community (and it's open-source!)

## Hardware

For good audio, my minimum requirements for hardware are:

- A dedicated soundboard
- A studio mic
- Some pop-filter (a sock is a great option)
- A fairly sound absorbing room

# Audio levels

## Recording

When recording, audio levels should never go over 0 db.

To prevent that, I aim for the audio levels to bounce around -12 db, so I have some headroom if the audio sometimes get loud occassionaly.

## Editing

The audio levels will change all the time during editing, but my end-goal is to have the peak levels just below 0 (I aim for maybe -1 db).

During editing, I will try to balance the audio level of a clip so the volume is more or less the same throughout, without removing all of the dynamics.

# Edit steps

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
