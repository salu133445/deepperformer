Deep Performer is a novel three-stage system for score-to-audio music performance synthesis. It is based on a transformer encoder-decoder architecture commonly used in text-to-speech synthesis. In order to handle polyphonic music inputs, we propose a new _polyphonic mixer_ for aligning the encoder and decoder. Moreover, we propose a new _note-wise positional encoding_ for providing a fine-grained conditioning to the model so that the model can learn to behave differently at the beginning, middle and end of a note.

## Dataset

To train our proposed system, we compile a new dataset of 6.5 hours of professional violin recordings along with their scores and estimated alignments. The dataset and the source code for the alignment process can be found [here](https://salu133445.github.io/bach-violin-dataset/).

## Audio samples

- Some samples synthesized by our proposed model can be found below.
- Audios for the figures on the paper are available [here](examples).
- Audio samples for the subjective listening test can be found [here](violin) (violin) and [here](piano) (piano).

| Violin | Piano |
|:-:|:-:|
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1002_mov2_009.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1003_mov2_004.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1006_mov1_033.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_karen-gomyo_bwv1006_mov4_012.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_oliver-colbentson_bwv1006_mov7_006.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |

## Paper

__Deep Performer: Score-to-Audio Music Performance Synthesis__<br>
<small>
Hao-Wen Dong, Cong Zhou, Taylor Berg-Kirkpatrick, and Julian McAuley<br>
_Proceedings of the IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)_, 2022<br>
[[homepage](https://github.com/salu133445/deepperformer)] [[reviews](https://github.com/salu133445/deepperformer/pdf/deepperformer-icassp2022-reviews.pdf)]
</small>
