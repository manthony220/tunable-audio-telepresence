# Head-Tracked Tunable Audio Telepresence — Supplementary Material

Listening examples, spectrograms and video demonstrations for:

> **A Head-Tracked Tunable Audio Telepresence System Based on the Generalized Model-Matching Sound Field Analysis and Synthesis Framework**
> Shu-Yi Yang, Michael Anthony, Mingsian R. Bai
> National Tsing Hua University, Hsinchu, Taiwan

**▶ Listen here: https://USERNAME.github.io/REPONAME/**

## What is here

The same test utterance reproduced in the three modes of the proposed system —
Enhancement Mode (α = 0), Mixture Mode (α = 0.5) and Immersion Mode (α = 1) —
under the unprocessed condition, the desired target, the DSP-based baseline and
the proposed mSEMamba model, together with the corresponding spectrograms.

The videos show the complete system running end to end, from far-end analysis
through near-end reproduction. In each clip a talker walks out of the far-end
target zone roughly twenty seconds in: her voice is suppressed to silence in
EM, attenuated but audible in MM, and preserved unchanged in IM.

The listening examples were produced under a far-end reverberation time of
T60 = 400 ms, at an SNR of 17 dB and an SIR of 0.88 dB.

**Use headphones.** The audio files are binaural ear signals; the interaural
cues they demonstrate do not survive playback over loudspeakers.

## Layout

```
index.html          the demo page
audio/              16 kHz, 16-bit stereo WAV, 5.00 s each
figures/            spectrograms, 0–8 kHz, −100 to 0 dB
video/              1080p H.264, 35 s each
```

Audio file names are `<mode>_<condition>.wav`, with `<mode>` one of `em`, `mm`,
`im` and `<condition>` one of `desired`, `dsp`, `msemamba`. The unprocessed
condition does not depend on α and appears once, as `audio/unprocessed.wav`.

## Levels

The nine ear-signal files carry their **true relative levels**. No per-file
normalisation and no loudness matching have been applied, so level differences
between conditions and between modes are part of the result rather than an
artefact of preparation. Set a comfortable volume on one file and leave it
there for the rest.

`unprocessed.wav` is the exception: it holds microphones 1 and 5 of the
eight-element far-end array, which are microphone signals rather than ear
signals and therefore not on the same scale. Its level has been set to match
the IM desired signal so that it sits sensibly alongside the others. In the
paper this condition is evaluated after reproduction over the loudspeakers.

## Source material and licensing

The mixtures are built from three corpora, each under its own licence:

- Test speech — [CSTR VCTK Corpus](https://datashare.ed.ac.uk/handle/10283/3443)
- Training and validation speech — [LibriSpeech](https://www.openslr.org/12)
- Background noise — [WHAM!](http://wham.whisper.ai/)

The media in this repository are released under
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/), the most
restrictive of the terms attaching to the underlying corpora. **Verify each
corpus's current licence before relaxing this** — in particular, confirm
whether WHAM!'s non-commercial clause still applies, since that is what sets
the terms here.

## Publishing the page

The site is plain static HTML with no build step.

1. Push this directory to a GitHub repository.
2. **Settings → Pages → Source:** Deploy from a branch, `main`, `/ (root)`.
3. Replace `USERNAME/REPONAME` in the link above with the real path, and fill
   in the paper link in `index.html` (search for `link to appear`).

## Citation

```bibtex
@article{yang_tunable_telepresence,
  title   = {A Head-Tracked Tunable Audio Telepresence System Based on the
             Generalized Model-Matching Sound Field Analysis and Synthesis Framework},
  author  = {Yang, Shu-Yi and Anthony, Michael and Bai, Mingsian R.},
  journal = {Discover Robotics},
  year    = {2026}
}
```

## Acknowledgment

Supported by the National Science and Technology Council (NSTC) under grant
113-2221-E-007-057-MY3.
