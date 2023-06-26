__Deep Performer: Score-to-Audio Music Performance Synthesis__
{:.center .larger}

[Hao-Wen Dong](https://salu133445.github.io/)<sup>1,2</sup> &emsp;
[Cong Zhou](https://www.linkedin.com/in/cong-zhou-93427426/)<sup>1</sup> &emsp;
[Taylor Berg-Kirkpatrick](https://cseweb.ucsd.edu/~tberg/)<sup>2</sup> &emsp;
[Julian McAuley](https://cseweb.ucsd.edu/~jmcauley/)<sup>2</sup>\\
<sup>1</sup> Dolby Laboratories &emsp;
<sup>2</sup> University of California San Diego\\
<span style="font-size: smaller;">\* Work done during an internship at Dolby</span>
{:.center}

{% include icon_link.html text="paper" icon=site.icons.paper href="https://arxiv.org/pdf/2202.06034.pdf" %} &emsp;
{% include icon_link.html text="demo" icon=site.icons.demo href="https://salu133445.github.io/deepperformer/" %} &emsp;
{% include icon_link.html text="video" icon=site.icons.video href="https://youtu.be/DeV23I_vOA8" %} &emsp;
{% include icon_link.html text="slides" icon=site.icons.slides href="https://salu133445.github.io/deepperformer/pdf/deepperformer_icassp2022_slides.pdf" %} &emsp;
{% include icon_link.html text="poster" icon=site.icons.poster href="https://salu133445.github.io/deepperformer/pdf/deepperformer_icassp2022_poster.pdf" %} &emsp;
{% include icon_link.html text="reviews" icon=site.icons.reviews href="https://salu133445.github.io/deepperformer/pdf/deepperformer_icassp2022_reviews.pdf" %}
{:.center}

{% include youtube_player.html id="DeV23I_vOA8" %}

---

## Content

- [Best samples](#best-samples)
- [Datasets](#datasets)
- [Violin samples](#violin)
- [Piano samples](#piano)
- [Audios for the figures on the paper](#figures)
- [Citation](#citation)

---

## Best samples {#best-samples}

| Violin | Piano |
|:-:|:-:|
| {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1002_mov2_009.wav" %} | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1003_mov2_004.wav" %} | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1006_mov1_033.wav" %} | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_karen-gomyo_bwv1006_mov4_012.wav" %} | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_oliver-colbentson_bwv1006_mov7_006.wav" %} | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |

---

## Datasets {#datasets}

We used two datasets to train our proposed system: [Bach Violin Dataset](https://salu133445.github.io/bach-violin-dataset/) for the violin and [MAESTRO Dataset](https://magenta.tensorflow.org/datasets/maestro) for the piano.

The Bach Violin Dataset is a collection of high-quality public recordings of Bach’s sonatas and partitas for solo violin (BWV 1001–1006). The dataset consists of 6.5 hours of professional recordings from 17 violinists recorded in various recording setups. It also provides the reference scores and estimated alignments between the recordings and scores. Below is an example of the alignment provided, where white dots and green lines show the estimated note onsets and durations.

![alignment](img/alignment.jpg)

{% include audio_player.html filename="audio/emil-telmanyi_bwv1001_trimmed_30sec.mp3" %}

_For more information, please visit the project [website](https://salu133445.github.io/bach-violin-dataset/) for the Bach Violin Dataset._

---

## Violin samples {#violin}

> These are the violin samples used in the subjective listening test. We used the [Bach Violin Dataset](https://salu133445.github.io/bach-violin-dataset/) to train our models.

### (V1) Bach - Violin Partita no. 1 in B minor, BWV 1002, mov. 2 - Emil Telmányi

| Baseline                                     | {% include audio_player.html filename="audio/violin/hifigan/hifigan_emil-telmanyi_bwv1002_mov2_009.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1002_mov2_009.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/violin/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_emil-telmanyi_bwv1002_mov2_009.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/violin/fastspeech-no-performer-emb/fastspeech-no-performer-emb_emil-telmanyi_bwv1002_mov2_009.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/violin/fastspeech-pianoroll/fastspeech-pianoroll_emil-telmanyi_bwv1002_mov2_009.wav" %} |

### (V2) Bach - Violin Partita no. 1 in B minor, BWV 1002, mov. 2 - Emil Telmányi

| Baseline                                     | {% include audio_player.html filename="audio/violin/hifigan/hifigan_emil-telmanyi_bwv1003_mov2_004.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1003_mov2_004.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/violin/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_emil-telmanyi_bwv1003_mov2_004.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/violin/fastspeech-no-performer-emb/fastspeech-no-performer-emb_emil-telmanyi_bwv1003_mov2_004.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/violin/fastspeech-pianoroll/fastspeech-pianoroll_emil-telmanyi_bwv1003_mov2_004.wav" %} |

### (V3) Bach - Violin Partita No. 3 in E major, BWV 1006, mov. 1 - Emil Telmányi

| Baseline                                     | {% include audio_player.html filename="audio/violin/hifigan/hifigan_emil-telmanyi_bwv1006_mov1_033.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1006_mov1_033.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/violin/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_emil-telmanyi_bwv1006_mov1_033.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/violin/fastspeech-no-performer-emb/fastspeech-no-performer-emb_emil-telmanyi_bwv1006_mov1_033.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/violin/fastspeech-pianoroll/fastspeech-pianoroll_emil-telmanyi_bwv1006_mov1_033.wav" %} |

### (V4) Bach - Violin Partita No. 3 in E major, BWV 1006, mov. 4 - Karen Gomyo

| Baseline                                     | {% include audio_player.html filename="audio/violin/hifigan/hifigan_karen-gomyo_bwv1006_mov4_012.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_karen-gomyo_bwv1006_mov4_012.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/violin/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_karen-gomyo_bwv1006_mov4_012.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/violin/fastspeech-no-performer-emb/fastspeech-no-performer-emb_karen-gomyo_bwv1006_mov4_012.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/violin/fastspeech-pianoroll/fastspeech-pianoroll_karen-gomyo_bwv1006_mov4_012.wav" %} |

### (V5) Bach - Violin Partita No. 3 in E major, BWV 1006, mov. 7 - Oliver Colbentson

| Baseline                                     | {% include audio_player.html filename="audio/violin/hifigan/hifigan_oliver-colbentson_bwv1006_mov7_006.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/violin/fastspeech-full/fastspeech-full_oliver-colbentson_bwv1006_mov7_006.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/violin/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_oliver-colbentson_bwv1006_mov7_006.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/violin/fastspeech-no-performer-emb/fastspeech-no-performer-emb_oliver-colbentson_bwv1006_mov7_006.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/violin/fastspeech-pianoroll/fastspeech-pianoroll_oliver-colbentson_bwv1006_mov7_006.wav" %} |

---

## Piano samples {#piano}

> These are the piano samples used in the subjective listening test. We used the [MAESTRO Dataset](https://magenta.tensorflow.org/datasets/maestro) to train our models.

### (P1) International Piano-e-Competition 2006

| Baseline                                     | {% include audio_player.html filename="audio/piano/hifigan/hifigan_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/piano/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/piano/fastspeech-no-performer-emb/fastspeech-no-performer-emb_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/piano/fastspeech-pianoroll/fastspeech-pianoroll_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |

### (P2) International Piano-e-Competition 2008

| Baseline                                     | {% include audio_player.html filename="audio/piano/hifigan/hifigan_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/piano/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/piano/fastspeech-no-performer-emb/fastspeech-no-performer-emb_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/piano/fastspeech-pianoroll/fastspeech-pianoroll_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |

### (P3) International Piano-e-Competition 2009

| Baseline                                     | {% include audio_player.html filename="audio/piano/hifigan/hifigan_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/piano/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/piano/fastspeech-no-performer-emb/fastspeech-no-performer-emb_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/piano/fastspeech-pianoroll/fastspeech-pianoroll_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |

### (P4) International Piano-e-Competition 2011

| Baseline                                     | {% include audio_player.html filename="audio/piano/hifigan/hifigan_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/piano/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/piano/fastspeech-no-performer-emb/fastspeech-no-performer-emb_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/piano/fastspeech-pianoroll/fastspeech-pianoroll_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |

### (P5) International Piano-e-Competition 2013

| Baseline                                     | {% include audio_player.html filename="audio/piano/hifigan/hifigan_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |
| Deep Performer (ours)                        | {% include audio_player.html filename="audio/piano/fastspeech-full/fastspeech-full_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |
| &emsp;- w/o note-wise positional encoding    | {% include audio_player.html filename="audio/piano/fastspeech-no-note-pos-enc/fastspeech-no-note-pos-enc_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |
| &emsp;- w/o performer embedding              | {% include audio_player.html filename="audio/piano/fastspeech-no-performer-emb/fastspeech-no-performer-emb_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |
| &emsp;- w/o encoder (using piano roll input) | {% include audio_player.html filename="audio/piano/fastspeech-pianoroll/fastspeech-pianoroll_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |

---

## Audios for the figures on the paper {#figures}

### Figure 1

An overview of the proposed three-stage pipeline for score-to-audio music performance synthesis.

![overview](img/overview.png){: style="max-height: 200px; width: auto;"}

{% include audio_player.html filename="audio/emil-telmanyi_bwv1005_mov2_022.wav" %}

### Figure 3

An example of the constant-Q spectrogram of the first 20 seconds of a violin recording and the estimated onsets (white dots) and durations (green lines).

![alignment](img/alignment.png){: style="max-height: 200px; width: 600px; max-width: 100%;"}

{% include audio_player.html filename="audio/emil-telmanyi_bwv1001_trimmed.mp3" %}

### Figure 5

Examples of the mel spectrograms, in log scale, synthesized by our proposed model for (a) violin and (c) piano. (b) and (d) show the input scores for (a) and (c), respectively.

| (a) | ![synth-poly-violin](img/synth-poly-violin.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (b) | ![synth-poly-violin-input](img/synth-poly-violin-input.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="audio/fastspeech-full_emil-telmanyi_bwv1003_mov2_004.wav" %}

| (c) | ![synth-poly-piano](img/synth-poly-piano.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (d) | ![synth-poly-piano-input](img/synth-poly-piano-input.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="audio/MIDI-Unprocessed_09_R2_2009_01_ORIG_MID--AUDIO_09_R2_2009_09_R2_2009_01_WAV_057.wav" %}

### Figure 6

Examples of the mel spectrograms, in log scale, synthesized by (a) the baseline model, (b) our proposed synthesis model, and (d) our proposed synthesis model without the note-wise positional encoding. (c) and (e) show the waveforms for (b) and (d), respectively. (f) shows the input score.

| (a) | ![synth-comparison-baseline](img/synth-comparison-baseline.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="audio/hifigan_emil-telmanyi_bwv1002_mov2_009.wav" %}

| (b) | ![synth-comparison](img/synth-comparison-highlighted.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (c) | ![synth-comparison-waveform](img/synth-comparison-waveform-highlighted.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="audio/fastspeech-full_emil-telmanyi_bwv1002_mov2_009.wav" %}

| (d) | ![synth-comparison](img/synth-comparison-no-npe-highlighted.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (e) | ![synth-comparison-waveform](img/synth-comparison-no-npe-waveform-highlighted.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="audio/fastspeech-no-note-pos-enc_emil-telmanyi_bwv1002_mov2_009.wav" %}

---

## Citation {#citation}

> Hao-Wen Dong, Cong Zhou, Taylor Berg-Kirkpatrick, and Julian McAuley, "Deep Performer: Score-to-Audio Music Performance Synthesis," _Proceedings of the IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)_, 2022.

```bibtex
@inproceedings{dong2022deepperformer,
    author = {Hao-Wen Dong and Cong Zhou and Taylor Berg-Kirkpatrick and Julian McAuley},
    title = {Deep Performer: Score-to-Audio Music Performance Synthesis},
    booktitle = {Proceedings of the IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
    year = 2022,
}
```
