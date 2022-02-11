# Audios for the figures

These are the audios for the figures on the paper.

## Figure 1

An overview of the proposed three-stage pipeline for score-to-audio music performance synthesis.

![overview](assets/images/overview.png){: style="max-height: 200px; width: auto;"}

{% include audio_player.html filename="assets/audio/emil-telmanyi_bwv1005_mov2_022.wav" %}

## Figure 3

An example of the constant-Q spectrogram of the first 20 seconds of a violin recording and the estimated onsets (white dots) and durations (green lines).

![alignment](assets/images/alignment.png){: style="max-height: 200px; width: 600px; max-width: 100%;"}

{% include audio_player.html filename="assets/audio/emil-telmanyi_bwv1001_trimmed.mp3" %}

## Figure 5

Examples of the mel spectrograms, in log scale, synthesized by our proposed model for (a) violin and (c) piano. (b) and (d) show the input scores for (a) and (c), respectively.

| (a) | ![synth-poly-violin](assets/images/synth-poly-violin.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (b) | ![synth-poly-violin-input](assets/images/synth-poly-violin-input.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="assets/audio/fastspeech-full_emil-telmanyi_bwv1003_mov2_004.wav" %}

| (c) | ![synth-poly-piano](assets/images/synth-poly-piano.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (d) | ![synth-poly-piano-input](assets/images/synth-poly-piano-input.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="assets/audio/MIDI-Unprocessed_09_R2_2009_01_ORIG_MID--AUDIO_09_R2_2009_09_R2_2009_01_WAV_057.wav" %}

## Figure 6

Examples of the mel spectrograms, in log scale, synthesized by (a) the baseline model, (b) our proposed synthesis model, and (d) our proposed synthesis model without the note-wise positional encoding. (c) and (e) show the waveforms for (b) and (d), respectively. (f) shows the input score.

| (a) | ![synth-comparison-baseline](assets/images/synth-comparison-baseline.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="assets/audio/hifigan_emil-telmanyi_bwv1002_mov2_009.wav" %}

| (b) | ![synth-comparison](assets/images/synth-comparison-highlighted.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (c) | ![synth-comparison-waveform](assets/images/synth-comparison-waveform-highlighted.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="assets/audio/fastspeech-full_emil-telmanyi_bwv1002_mov2_009.wav" %}

| (d) | ![synth-comparison](assets/images/synth-comparison-no-npe-highlighted.png){: style="max-height: 100px; width: 600px; max-width: 100%;"} |
| (e) | ![synth-comparison-waveform](assets/images/synth-comparison-no-npe-waveform-highlighted.png){: style="max-height: 50px; width: 600px; max-width: 100%;"} |

{% include audio_player.html filename="assets/audio/fastspeech-no-note-pos-enc_emil-telmanyi_bwv1002_mov2_009.wav" %}
